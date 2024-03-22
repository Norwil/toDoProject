# todo-app

## Project setup
```
npm install
```

### Compiles and hot-reloads for development
```
npm run serve
```

### Compiles and minifies for production
```
npm run build
```

### Lints and fixes files
```
npm run lint
```

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).

### Template Section
```
`v-model="newTask"`: This creates a two-way binding on the input form element, linking it to the newTask data property.
`@keyup.enter="addTask"`: This is an event listener that calls the addTask method when the Enter key is pressed.
`@click="addTask"`: This is an event listener that calls the addTask method when the button is clicked.
v-for="task in tasks": This is a loop directive that renders a list item for each task in the tasks array.
`:key="task.id"`: Vue uses the key attribute to track each node’s identity, which is important for efficient dynamic node updating.
`v-model="task.completed"`: Two-way binding on the checkbox to toggle the completed state of a task.
`:class="{ completed: task.completed }"`: This dynamically binds the completed class to the span element if the task’s completed property is true.
`@click="removeTask(task.id)"`: Calls the removeTask method with the current task’s id when the button is clicked.
```
