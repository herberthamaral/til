regexp_replace with flags
=========================

25/02/2016

In PostgreSQL, `regexp_replace` usually takes three arguments: text, pattern
and replacement. But like JS, it is necessary to specify a global flag to
replace every pattern occurrence in the text, like this:

    postgres=# SELECT regexp_replace('the quick brown fox jumps over the lazy dog', '[aeiou]', '', 'g');
    regexp_replace          
    ----------------------------------
    th qck brwn fx jmps vr th lzy dg
    (1 row)

Without it the result would be like as follows:

    postgres=# SELECT regexp_replace('the quick brown fox jumps over the lazy dog', '[aeiou]', '');
    regexp_replace               
    --------------------------------------------
    th quick brown fox jumps over the lazy dog
    (1 row)

