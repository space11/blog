---
title: Using data attributes in React.
date: "2019-03-22T07:52:00"
author: "Borys"
---

## React Access

Add a custom data attribute in JSX:

```JavaScript
render() {
   <a data-custom={} onClick={this.handleClick}\>foo</a>
}
```

Access it:

```JavaScript
handleClick(event) {
	const customData  = event.target.attributes.getNamedItem('data-custom').value;
	console.write('data-custom: ', customData)
}
```

## JavaScript access

Add custom data attributes in HTML:

```HTML
<article
  class="js-post-1"
  data-columns="3"
  data-index-number="12314"
  data-parent="cars">
  ...
</article>
```

Use it in JavaScript:

```JavaScript
const post = document.querySelector('.js-post-1');
post.dataset.columns // "3"
post.dataset.indexNumber // "12314"
post.dataset.parent // "cars"

```

## CSS access

Use the attribute selectors in CSS to change styles according to the data:

```CSS
	article[data-columns='3'] {
	width: 400px;
}
article[data-columns='4'] {
	width: 600px;
}
}
```
