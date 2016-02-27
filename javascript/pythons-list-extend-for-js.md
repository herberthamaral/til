Python's list.extend for JS
===========================

2016-02-27

I found myself doing something like

    someArray.forEach(function(a) { anoterArray.push(a) })

And I thought I was being silly (and indeed I was). There is a smarter way to do it using [apply](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function/apply):

    $ node
    > var someArray = [1,2,3]
    undefined
    > var anotherArray = [4,5,6]
    undefined
    > anotherArray.push.apply(anotherArray, someArray)
    6
    > anotherArray
    [ 4, 5, 6, 1, 2, 3 ]

