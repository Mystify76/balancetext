Usage:

`import balanceText                  from "@mystify/balancetext";`

To have the library load all the elements with the "balance-text" class name call "balanceText" in the did mount. I found that I have to update the watched elements after the mount to make sure that it picks up and adjusts the elements after the first render

```
componentDidMount() {  
    balanceText();  
    requestAnimationFrame(()=>balanceText.updateWatched());  
}

render() {
    // add the class name "balance-text" to your component to make it work
    return <span className="balance-text">This is my text</span>

}
```
