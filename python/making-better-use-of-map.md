Making better use of map
========================


I personally tend to overuse Python's list comprehension, even when `map` would
do a better job at keeping the code smaller and maybe more readable. Consider
this trivial example:

    data = ['-0.1', '35.1', '5.3', '12.3', '1.5']
    data = [float(d) for da in data]

The very same can (and probably should) be done like this:

    data = ['-0.1', '35.1', '5.3', '12.3', '1.5']
    data = map(float, data)

For what is worth the first `map` parameter can be any callable (like an instance method).
