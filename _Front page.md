## Global To-do's
Short term To-Dos that should get done of the course of a week or two at most. Oldest tasks are at the top unless a task contains the LP Tag

```dataview
TASK
FROM !"Templates"
WHERE !checked AND text != "" AND !contains(file.tags, "#LT") AND !contains(file.tags, "#tignore")
SORT contains(text, "#LP") ASC, file.ctime ASC
```


> [!warning]- Overdue Tasks
> ```dataview
> TASK FROM !"Templates"
> WHERE !checked AND text != "" AND !contains(file.tags, "#LT") AND !contains(file.tags, "#tignore") AND date(Due) < date(today) AND Due != null
> ```

## Currently Relevant

- 

### Needs Processing
```dataview
LIST from "Daily Notes" 
WHERE should-process = "true" AND processed = "false"
```

## Legend
### Tags
#maintenance ➡️ Maintenance: Tasks or information relating to maintenance of servers
#LP ➡️ Low Priority: this can be done at a time when it is convenient
#LT ➡️ Long Term: this is a long running to-do that can take weeks, months, or years to complete
#tignore  ➡️ Checklist items in tagged file are ignored for the front page Global To-dos
