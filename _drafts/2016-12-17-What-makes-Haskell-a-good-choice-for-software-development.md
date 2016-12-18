---
layout: post
title: What makes Haskell a good choice for software development
published: false
---

![Haskell logo](https://www.haskell.org/static/img/haskell-logo.svg?etag=ukf3Fg7- )
Haskell is my favorite language of choice. For those not familiar with it, it is a purely functional, statically typed, declarative language. 

Functions are the key citicens. We all know functions as something with some input and some output. Each time a function is used with the same input, you will get the same output. Like math. This is a very nice feature, because it makes reasoning about the correctness of the code fairly easy. There are no variables with changing values. Those changing values are a source of bugs in other languages. It is difficult to write loops and at the same time ensure that initialisation is done without errors. 

Ok. you want an example? Here it is:

    
    
{% highlight haskell linenos %}
intSort :: [Int] -> [Int]
intSort []       = []
intSort (i:rest) = [x | x <- rest, x < i]
                 ++[i]
                 ++
{% endhighlight %}
