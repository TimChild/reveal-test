## Notes on using revealjs slideshow

This is intended to be a quick reference for creating slideshows using revealjs.

This is somewhat specific to the way I have set up my workflow in my [dotfiles](https://github.com/TimChild/dotfiles) repository.
But most of it should be general enough for someone else using this too.

---

What if a slide has lots of content?

For example, it has lots of different lines of content...

<small>
Like this...

And this..

And this..

And this..

And this..

And this..

And this..

And this..

And this..

And this..

</small>

```markdown
use <small> tags to make text smaller </small>
```

---

## Creating a new slideshow

<small>
(This relies on my dotfiles setup)
</small>

```bash
task -g web:new-slideshow
```

<small>
This will create a new directory within the current directory with all the required files for a new slideshow.

To customize it, just start editing the `content/slides.md` file.

To run it:

```bash
cd new-slideshow && npm start -- --port 8000  # Port 8000 is default anyway
```

Optionally pass

```bash
task -g web:new-slideshow SUBDIR=sub/path
```

to chose the subdirectory within the current directory.

</small>

---

## Hotkeys

Press "?" to see the hotkeys.

For example, enter "S"peaker mode to pop out a speaker view where slide notes can also be seen.

note:

- Any notes after `note:` or `Notes:` will be displayed in the speaker notes only.

---

## Embedding images

Embed an image using the usual markdown syntax.

```markdown
![Image](https://picsum.photos/500/300)
```

This produces:

![Image](https://picsum.photos/500/300)

===

### Vertical slide under second slide

---

## Showing code with highlighting

````markdown
```python [1|2-3|]
def example_code():
    print("Hello, World!")
    #  comment
    return "Hello, World!"
```
````

produces:

```python [1|2-3|]
def example_code():
    print("Hello, World!")
    #  comment
    return "Hello, World!"
```
