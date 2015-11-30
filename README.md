# task-manager-cli
```
These commands provide the basic support for a multi-tasking pool of workers, their manager as well as the business users that are submitting tasks that need to be done.

The business user typically adds tasks via `add`.
The business user can cancel a task via `delete`
The business user can see the status of a specific task via `show`
The business user can see summary info about the state of the tasks they have submitted via `list`

The worker can denote their availability to work on the task by issuing a `login` 
The worker can fetch a task and start working on it by issuing a `grab`
They can see (without fetching) the next task in the queue by issuing a `peek`
They can fetch a task while working on a task using consecutive `grab`s.  Doing so suspends the prior task
the worker was working on, but still leaves it in their control. The worker can have multiple
suspended tasks  but only one of them is the task actively being worked on - only that task is accumulating work-time.
The worker can see the tasks under their control by issuing a `jobs`
The worker can bring a task into the foreground by issuing a `fg` - that automatically suspends the current task.
The worker can suspend their current task by issying `bg` - the worker can take a break - making sure that no task is accumulating work-time
The worker can return the task to the queue without completing it by issuing a `release`
The worker can complete a task by issuing a `done` 
Both `done` and `delete` are final operations. ie they represent final states for the task
A worker can leave the pool of available workers by issuing a `logout`

The team manager can see the currently active users by issuing a `who`
The team manager can take over a worker account (e.g. to release the workers tasks) by issuing a `sudo`
The team manager can see information about a workers whereabouts by issuing a `finger`
The team manager can see the last login/logouts by issuing a `last`
The team manager can see the last commands issued by people by issuing a `lastcomm`
```


