---
StartDate: <% tp.date.now("YYYYMMDD") %>
EndDate: ""
Title: ChangeMe
Useful: false
Paper-worthy: false
Completed: false
---
<%* 
let d = tp.date.now("YYYYMMDD");
let label = "PJMS";
let index = 1;
let extension = ".md"
console.log("start:");
let name = d + "_" + label + ('00' + index).slice(-2);

function renameFile(newName) {
  possibleLoc = "experiments/" + newName + extension
  console.log("possibleLoc is: " + possibleLoc)
  return tp.file.exists(possibleLoc)
    .then((exists) => {
      if (exists) {
        console.log("possibleLoc rejected")
        index = index + 1;
        newName = d + "_" + label + ('00' + index).slice(-2);
        // Update the name variable with the new name here
        name = newName;
        return renameFile(newName);
      } else {
	    console.log("Will now rename:", name);
        return tp.file.rename(newName);
      }
    });
}

renameFile(name)
  .then(() => {
    console.log("Successfully renamed:", name);
  })
  .catch((error) => {
    console.error("Error:", error);
  });
%>

## Goal & background
Previous and related experiments:

## Procedure


## Results & Takeaway
