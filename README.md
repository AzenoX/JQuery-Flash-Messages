# JQuery Flash Messages

This little script allows you to add flash messages to your web pages.

## Getting Started

### JQuery

First, you have to import JQuery (for now, it's required).

```
<script type="text/javascript" src="https://cdnjs.cloudflare.com/ajax/libs/jquery/3.3.1/jquery.min.js"></script>
```

### Sources

Then import src/ files.

```
<link rel="stylesheet" type="text/css" href="flash.css">
<script src="flash.js"></script>
```

## Usage


### On Page Load

Creating a flash message (span element is used to add close button):

```
<div class="flash">This is a flash message !<span></span></div>
```

These messages triggers when the page load.


### On Click

Create the flash message:

```
<div id="flash--test" class="flash">This is a flash message.<span></span></div>
```
You need to add an ID (here 'flash--test').

Now, you have to create the button:

```
<button class="flash--activate" data-activate="flash--test">Open Flash Test</button>
```

These messages triggers when the button is clicked.


### On Event

Create the flash message:

```
<div id="flash--test" class="flash">This is a flash message.<span></span></div>
```

Simply use this JS function:

```
flash_trigger(element_id, false);
```


## Custom Flash Message Duration

### Change Duration

Normally, flash messages disappear after 5 seconds. If you want to change this, just add one argument:

```
flash_trigger(element_id, false, TIME_IN_MILLISECONDS);
```

Example:

```
flash_trigger(element_id, false, 10000); //10 Seconds
```

### Permanent by JS

Or, if you want to have a permanent message, closable by click on the close button:

```
flash_trigger(element_id, true); //Unlimited
```

### Permanent by HTML

Or, if you want to have a permanent message, closable by click on the close button:

```
<div class="flash flash--permanent">This is a flash message.<span></span></div>
```

## Style

You just need to add a defined class, and you can of course create your owns.

### Success Message

```
<div class="flash flash-success">This is a success flash message.<span></span></div>
```

### Error Message

```
<div class="flash flash-error">This is an error flash message.<span></span></div>
```


## Licensing

You are allowed to use, modify, redistribute this, as you want.