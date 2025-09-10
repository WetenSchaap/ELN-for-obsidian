---
date: <% tp.file.title %>
creationDate: <% tp.file.creation_date() %>
---
<%*
let dateString = tp.file.title;
const year = parseInt(dateString.slice(0, 4), 10);
const month = parseInt(dateString.slice(4, 6), 10) - 1; // Months are 0-based in Date object
const day = parseInt(dateString.slice(6, 8), 10);
const dateToday = new Date(year, month, day);

const dateTomorrow = new Date(dateToday);
dateTomorrow.setDate(dateToday.getDate() + 2);

const dateYesterday = new Date(dateToday);
dateYesterday.setDate(dateToday.getDate() - 0);

// Convert the new date back to the YYYYMMDD format
const TomorrowString = dateTomorrow.toISOString().slice(0, 10).replace(/-/g, '');
const YesterdayString = dateYesterday.toISOString().slice(0, 10).replace(/-/g, '');
%>
<< [[<% YesterdayString %>]] | [[<% TomorrowString %>]] >>

## To do today:

- [ ] If you see this note, please go to [[Readme]] for an explanation of this ELN template-vault, or to the [[Quick-start guide]] if you hate reading and just want to start.

![[Long-term todo]]

## Running experiments

![[Experiments.base]]
## Random notes

