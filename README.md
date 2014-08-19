Grunt task for background styles processing.

## Description

This is just a small grunt task which generates @media styles for retina images.
It allows to avoid writing extra styles.

## Installation

To install it you can simply clone it to your project node modules.

## Usage example

You can see usage example below. There are several demos also in repo.
Here is the task configuration example.

```javascript
"retinify": {
    "single": {
        "options": {
            // img1.jpg generates link to img1-x2.jpg
            "retinaPrefix": '-x2',
            // output file name (to write all generated styles into single file)
            "resultsCSSFileName": 'media.css' 
        },
        "cwd": 'demo/src',
        "dest": 'demo/out',
        "src": ['*.css']
    }
}
```
Input css files examples:

styles1.css:

```css
.class-name2 > #some-id, .new-class {
    background: url('/demo/img/fxt1.gif');
}
```

styles2.css:

```css
.class-name2 > #some-id, .new-class {
    background-image: url('/demo/img/fxt2.gif');
}
```

Processing result is going to look like this.
media.css:

```css
@media (x2) {
    .class-name2 > #some-id, .new-class {
        background: url('/demo/img/fxt1-x2.gif');
    }
    .class-name2 > #some-id, .new-class {
        background-image: url('/demo/img/fxt2-x2.gif');
    }
}
```

## Options

Coming soon...

## License

MIT
