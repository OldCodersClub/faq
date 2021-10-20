# Markdown basic syntax #

origin: [Writing on GitHub](https://help.github.com/en/github/writing-on-github)

---

## Text ##

`**bold**` or `__bold__`  
**bold** or **bold**

---

`*italic*` or `_italic_`  
*italic* or _italic_

---

`***bold italic***`  
***bold italic***

---

`~~wrapped~~`  
~~wrapped~~

---

`_You **can** combine them_`  
_You **can** combine them_

---

`\**Ignoring\** \_Markdown\_ \~~formatting\~~`  
\**Ignoring\** \_Markdown\_ \~~formatting\~~

---

## URLs ##

_code:_  
`http://www.github.com/`

_result:_  
http://www.github.com/

---

_or_

_code:_  
`[link to Google!](http://google.com)`

_result:_  
[link to Google!](http://google.com)

---

_or with **title**:_

_code:_  
`[link to Google!](http://google.com "Goooooooooogle")`

_result:_  
[link to Google!](http://google.com "Goooooooooogle")

---

## Lists ##

##### Ordered: #####

```
1. Item 1
1. Item 2
1. Item 3
   1. Item 3a
      1. Item 3b
```

_result:_

1. Item 1
1. Item 2
1. Item 3
    1. Item 3a
        1. Item 3b

---

##### Unordered: #####

```
* Item 1
* Item 2
  * Item 2a
    * Item 2b
```

_result:_

* Item 1
* Item 2
    * Item 2a
        * Item 2b

---

_or_

```
- Item 1
- Item 2
  - Item 2a
    - Item 2b
```

_result:_

- Item 1
- Item 2
    - Item 2a
        - Item 2b

---

## Headers ##

`# Header 1` or `# Header 1 #`

# Header 1

---

`## Header 2` or `## Header 2 ##`

## Header 2

---

`### Header 3` or `### Header 3 ###`

### Header 3

---

`#### Header 4` or `#### Header 4 ####`

#### Header 4

---

`##### Header 5` or `##### Header 5 #####`

##### Header 5

---

`###### Header 6` or `###### Header 6 ######`

###### Header 6

---

## Quote ##

```
> Coffee. The finest organic suspension ever devised... I beat the Borg with it.
> - Captain Janeway
```

_result:_

> Coffee. The finest organic suspension ever devised... I beat the Borg with it.
> - Captain Janeway

---

## Code

_Inline code:_

```
string: `var example = true`
```

_result:_

string: `var example = true`

---

_block of code:_

&#96;&#96;&#96;  
if (isAwesome){  
&nbsp;&nbsp;&nbsp;&nbsp;return true }  
&#96;&#96;&#96;

_result:_

```
if (isAwesome){  
    return true
}
```

---

_syntax highlighting:_

&#96;&#96;&#96;python  
def foo(bar):  
&nbsp;&nbsp;&nbsp;&nbsp;if not bar:  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;return True  
&#96;&#96;&#96;

_result:_

```python
def foo(bar):
    if not bar:
        return True
```

---

## Task Lists

```
- [x] @mentions, #refs, [links](), **formatting**, and <del>tags</del> supported
- [x] list syntax required (any unordered or ordered list supported)
- [x] this is a complete item
- [ ] this is an incomplete item
```

_result:_

- [x] @mentions, #refs, [links](), **formatting**, and <del>tags</del> supported
- [x] list syntax required (any unordered or ordered list supported)
- [x] this is a complete item
- [ ] this is an incomplete item

---

## Tables

_code:_

```
First Header | Second Header
------------ | -------------
Content from cell 1 | Content from cell 2
Content in the first column | Content in the second column
```

_result:_

First Header | Second Header
------------ | -------------
Content from cell 1 | Content from cell 2
Content in the first column | Content in the second column

---

_or_

_code:_

```
| Left-aligned | Center-aligned | Right-aligned |
| :---         |     :---:      |          ---: |
| git status   | git status     | git status    |
| git diff     | git diff       | git diff      |
```

_result:_

| Left-aligned | Center-aligned | Right-aligned |
| :---         |     :---:      |          ---: |
| git status   | git status     | git status    |
| git diff     | git diff       | git diff      |

---

_or_

_code:_

```
| Name     | Character |
| ---      | ---       |
| Backtick | `         |
| Pipe     | \|        |
```

_result:_

| Name     | Character |
| ---      | ---       |
| Backtick | `         |
| Pipe     | \|        |

---

## Images

_code:_

```
![Image of Yaktocat](https://github.com/fluidicon.png)
```

_result:_

![Image of Yaktocat](https://github.com/fluidicon.png)

---

## Emoji

[emoji-cheat-sheet](https://github.com/ikatyang/emoji-cheat-sheet/blob/master/README.md)

https://www.webfx.com/tools/emoji-cheat-sheet/
