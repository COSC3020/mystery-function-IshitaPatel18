[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-24ddc0f5d75046c5622901739e7c5dd533143b0c8e959d652212380cedb1ea36.svg)](https://classroom.github.com/a/GDPVb20V)
# Mystery Function

What does the `mystery()` function in the following piece of code do? Add your
answer to this markdown file.

```javascript
function mystery(a) {
    if(a.length == 1) return a[0];
    var foo = mystery(a.slice(1, a.length))
    if(foo > a[0]) return foo;
    else return a[0];
}
```

My answer:
The code is looking for the greatest value in the array using recursion. Mystery is repeatedly called using the subarrays until
the termination case is reached, which returns the last element in the array (makes it equal to foo), and then checks it with a[0] in the previous
recursive call to see if it is greatest. If it is, foo returned for the previous call, if not a[0] is returned for the previous call, which makes
it equal to foo. This continues until the original function call, which produces the greatest value in the array.
