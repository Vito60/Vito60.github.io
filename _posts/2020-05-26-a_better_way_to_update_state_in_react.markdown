---
layout: post
title:      "A Better Way to Update State in React"
date:       2020-05-26 23:57:30 +0000
permalink:  a_better_way_to_update_state_in_react
---


In my example component the functionality I want to achieve is when a like button is clicked to increment the count of likes by one. My initial state, button, and handleClick function looks like this.
```
state = {
    likes: 0
  }
```

```
 <Button onClick={this.handelClick}> LIKE</Button>
```

```
handelClick = () => {
    this.setState({likes: this.state.likes + 1})
  }
```
The functionality I desire to achieve will work with this code but can be prone to errors because of the way React works. When multiple setState() calls are made react may combine them into a single update because setState is asynchronous. This behavior can lead to errors and cause state updates to have inconsistent results because the value of state is not immediately changed. To avoid issues, we can use callback functions with setState instead. 
```
handelClick = () => {
    this.setState((state) => ({
      likes: state.likes + 1
    }));
  }
```


