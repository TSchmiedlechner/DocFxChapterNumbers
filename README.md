
A hacked together tool to add chapter numbers to a `toc.md` file as it is used by docfx.

Usage:

## Edit your `toc.md` file, reference content files as usual

For example:
    
```markdown
# Content
## [Chapter 1 - Introduction](docs/chapter1.md)
```
    
## Inside the content files add your headings as you would:

For example (inside `chapter1.md` from above):
    
```markdown
# Chapter 1 - Introduction
## More Information
## Even more information
```
    
3. Run the tool from this repo, for example:

```cmd
DocFxChapterNumbers.exe .\mydocs\toc.md .\output
```
    
The folder `output` will have the same (sub-)folders that `mydocs` had,
containing the same files, but the headings in `toc.md` will be numbered
as will be the headings in the content files that are referenced from `toc.md`.
    
For example:
    
```markdown
# Content
## [1. Chapter 1 - Introduction](docs/chapter1.md)
```
    
and
    
```markdown
# 1. Chapter 1 - Introduction
## 1.1. More Information
## 1.2. Even more information
```
   
