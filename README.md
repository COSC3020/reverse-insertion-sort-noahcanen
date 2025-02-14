# Reverse Insertion Sort

Consider the code for insertion sort we covered in class:

```javascript
function insertionSort(arr) {
  for(var i = 1; i < arr.length; i++) {
    var val = arr[i];
    var j;
    for(j = i; j > 0 && arr[j-1] > val; j--) {
      arr[j] = arr[j-1];
    }
    arr[j] = val;
  }
  return arr;
}
```

Change this function such that it works from the end of the array rather than
the beginning, `insertionSortReverse()` -- only the direction of
iterating over the elements is reversed, the array is still sorted the same way
(ascending). Add your code in `code.js`. Test your new function; I've provided
some basic testing code that uses [jsverify](https://jsverify.github.io/) in
`code.test.js`.

## Average-Case Time Complexity of Insertion Sort

In the lectures, we covered that insertion sort has best-case time complexity of
$\Theta(n)$ and worst-case time complexity of $\Theta(n^2)$. What is the
average-case time complexity ($\Theta$)?

Hint: Think about what happens in each iteration of the loop, and how often the
loop is executed. Keep in mind that for asymptotic analysis we don't care about
constant factors.

Describe your reasoning and the conclusion you've come to. Your reasoning is
most important -- you can easily find the answer, but you need to demonstrate
that you've understood the concept. Add your answer to this markdown file.

 I think the average case is $\Theta(n^2)$ because, except for the best-case scenario, it must do Both loops several times to sort the most basic unsorted array. Inside of normal insertion sort, the 1st loop goes from the back of the array to the front of the array, checking to see if each element is more than the element behind it and if it finds an element that is less than the one behind it moves that element back until it either gets to the end or finds an element that is more than it meaning that if the list is always sorted the 2nd loop will never activate but if the 2nd loop activates it might go through the entirety of the list to find were that element belongs essentially checking every element against every other element making the average case of insertion sort  $\Theta(n^2)$.

 For this assignment, I was able to do it entirely on my own with a little help looking up syntax from the Internet.

"I certify that I have listed all sources used to complete this exercise, including the use of any Large Language Models. All of the work is my own, except where stated otherwise. I am aware that plagiarism carries severe penalties and that if plagiarism is suspected, charges may be filed against me without prior notice."
