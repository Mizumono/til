# Binary Gap

## Exercise:
A binary gap within a positive integer N is any maximal sequence of consecutive zeros that is surrounded by ones at both ends in the binary representation of N.

For example, number 9 has binary representation 1001 and contains a binary gap of length 2. The number 529 has binary representation 1000010001 and contains two binary gaps: one of length 4 and one of length 3. The number 20 has binary representation 10100 and contains one binary gap of length 1. The number 15 has binary representation 1111 and has no binary gaps. The number 32 has binary representation 100000 and has no binary gaps.

Write a function: function solution(N);
that, given a positive integer N, returns the length of its longest binary gap. The function should return 0 if N doesn't contain a binary gap.

## Solution:

```javascript
function solution(N) {
    let strNumber = N.toString(2);
    let sequenceCounter = 0;
    let maxSequenceCounter = 0;

    for (let digit of strNumber) {
        if ( digit === '0' ) {
            sequenceCounter += 1;
        } else {
            maxSequenceCounter = Math.max(sequenceCounter, maxSequenceCounter);
            sequenceCounter = 0;
        }
    }

    return maxSequenceCounter;
}
```

[zsoltnagy.eu](http://www.zsoltnagy.eu/javascript-tech-interview-exercise-2-binary-gap-exercise-in-codility/)