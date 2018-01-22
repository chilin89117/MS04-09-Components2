# MS04-09-Components2
## Advanced components

![App.vue](../assets/a.png?raw=true)
![Exercise8.vue](../assets/b.png?raw=true)

**Note: edit `main.js` to switch between `App.vue` and `Exercise8.vue`**
## `App.vue`
* Uses `<keep-alive>` to maintain state of its child component
* Uses `<component :is="">` to dynamically switch among child components

### `Quote.vue` component
* Inserts data into named slots
	* `App.vue`: `<h3 slot="title">{{quoteTitle}}</h3>`
	* `Quote.vue`: `<slot name="title"></slot>`

### `New.vue` component
* Has a counter to keep track of its state
* Logs the following lifecycle hooks:
	* `activated()`
	* `deactivated()`
	* `destroyed()`

#### End of Section 9, lecture 130.

## `Exercise8.vue`
* Dynamically switches 3 child components
	* `Blue.vue`
	* `Green.vue`
	* `Red.vue` 
