# Inverted Index
> An inverted index is an index data structure storing a mapping from content, such as words or numbers, to its locations in a document or a set of documents.

In simple words, it is a hashmap like data structure that directs you from a word to a document or a web page.

#### What are the variations?
There are two types of inverted indexes:
1. Record-level inverted index
2. Word-level inverted index

A record-level inverted index contains a list of references to documents for each word.
A word-level inverted index additionally contains the positions of each word within a document.
The latter form offers more functionality, but needs more processing power and space to be created.

### Um... Example maybe?
Consider the following three lines as three independent documents:
```
Doc 1: "hello world",
Doc 2: "this article is based on inverted index"
Doc 3: "which is hashmap like data structure"
```

The resulting inverted index from the above example would like the following:
```
hello                (1, 1)
everyone             (1, 2)
this                 (2, 1)
article              (2, 2)
is                   (2, 3); (3, 2)
based                (2, 4)
on                   (2, 5)
inverted             (2, 6)
index                (2, 7)
which                (3, 1)
hashmap              (3, 3)
like                 (3, 4)
data                 (3, 5)
structure            (3, 6)
```
In the above representation of an inverted index, we're using a word level index. The words of the documents are the keys and the the values are the occurrences.

### What are the advantages?
1. Inverted index is to allow fast full text searches, at a cost of increased processing when a document is added to the database.
2. It is easy to develop.

### What are the disadvantages?
1. Large storage overhead and high maintenance costs on update, delete and insert.

### What are the applications?
It is the most popular data structure used in document retrieval systems, used on a large scale for example in search engines.


#### References
1. https://www.geeksforgeeks.org/inverted-index/