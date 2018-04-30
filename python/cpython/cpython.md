# Understanding the forces that drive Python

## About
I recently wanted to understand how Python evolves, where it is heading, how it compares to other languages. This article is what I came up with in trying to answer these questions. 

## Starting point: Talk of Armin Ronacher
The talk that got me on that track is the following by Armin Ronacher, who has been part of Pytho for a long time, but also works with other languages, such as Rust and Javascript. He provided me with a birds eye view on Python, that I was seeking out:

<iframe width="560" height="315" src="https://www.youtube.com/embed/IeSu_odkI5I?rel=0" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen>
</iframe>

### How Python is driven by CPython
His main point in this talk is that Python is too much oriented towards CPython. Its future is shaped by whatever CPython is able to deliver, even though there are Jython Pypy and some more implementations of Python that have different possibilties.

### How things could be different
He contrasted Python with Javascript. What is different there is that:
- a language standard, such as [ECMAScript](https://en.wikipedia.org/wiki/ECMAScript) that is constantly evolving and tries to reach a common ground
- a translation tool to program in the future and back translate, such as [babel](https://babeljs.io/)

### Python is not standardized: instead it is becoming ever broader

How can you get a quick overview on the evolving of the language?

We will look at:
- PEPs
- CPython and how the repo is structured
- a concrete example such csv reading and writing

## PEPs describe what is behind the language constructs
When experienced Python people want to know what is going on in the language or what is new in a new release they look at PEPs.

Let's

## The example of csv files
I chose that example, because its scope is limited and the task and methods are easy to understand.

### csv did start as an independent module
- that was back in 2001 [csv module](http://www.object-craft.com.au/projects/csv/news.html#20021120)

###  PEP 305 -- CSV File API
since this is an easy topic, there is only one PEP regarding that topic: [PEP 305](https://www.python.org/dev/peps/pep-0305/)

- it was started in 2003 and all updates are from that year.
- notice that there is a section in the PEP on "To Do (Notes for the Interested and Ambitious)". I wonder whether that has ever been coded?

#### PEPS are the better documentation
I think in order to understand Python it is often better to read the PEPs: in this PEP, we learn:
- the history about why csv handling has become part of the standard library and what has been there before
- the interface: what are the important methods, that should be covered by that module

#### The history
- CSV Files used to come in many shapes and formats, such the "V" was considered to stand for "vague"
- there were different incompatible modules handling them up to that time being used by the Python community
- the PEP was a proposal to standardize these approaches

#### The Interface
Three APIs were needed regarding csv files:
- reading
- writing 
- sniffing: finding out what format the file was written in

> This PEP supports three basic APIs, one to read and parse CSV files, one to write them, and one to identify different CSV dialects to the readers and writers.


