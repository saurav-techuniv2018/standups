---
theme: "simple"
transition: "zoom"
progress: "true"
touch: "true"
mouseWheel: true
---

# `require()`

---

## Why do we need it?
<aside class="notes">We want to import other libraries and also make sure that our code is distributed across files to make it testable.</aside>

---

## How does it work?
<aside class="notes">Now, let us take a look at how this works.</aside>

---

# `module.js`
<aside class="notes">To understand require, we have to look at Node's module system in a file called module.js.  require function is a wrapper around a </aside>

---

## `Module._load`
<aside class="notes">require is a wrapper around the _load method. So, what does _load do?</aside>

---

# 1.
Check the cache for the requested file.

---

# 2.
If a module already exists in the cache: return its exports object.

---

# 3.
If the module is native: call `NativeModule.require()` with the filename and return the result.

---

# 4.
Otherwise, create a new module for the file and save it to the cache.

---

# 5. 
Then have it load the file contents before returning its exports object.

---

## But how do we get the exports object?

---

## `Module._compile`

---

```
Module._compile 
// Run the file contents in the correct scope or sandbox. Expose
// the correct helper variables (require, module, exports) to
// the file.
// Returns exception, if any.
```

---

# The Code

---


# JavaScript is awesome!

`Made with reveal.js`

---

# References

- http://fredkschott.com/post/2014/06/require-and-the-module-system/
- https://nodejs.org/api/addons.html
- https://revealjs.com/

---

# Questions?