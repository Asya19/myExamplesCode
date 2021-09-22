```
'use strict';

const pow = (x, n) => {
    return (n == 1) ? x : (x * pow(x, n - 1));
}

const factorial = (n) => {
    return (n == 1 || n == 0) ? 1 : (n * factorial(n - 1));
}

const sumTo = (n) => {

    return (n == 0 || n == 1) ? 1 : (n + sumTo(n - 1));
};

function fib(n) {
    return n <= 1 ? n : fib(n - 1) + fib(n - 2);
}

let list = { value: 1 };
list.next = { value: 2 };
list.next.next = { value: 3 };
list.next.next.next = { value: 10 };

let list2 = {
    value: 1,
    next: {
        value: 2,
        next: {
            value: 3,
            next: {
                value: 4,
                next: null
            }
        }
    }
};


const printList = (list) => {

    let tmp = list;

    while (tmp) {
        console.log(tmp.value);
        tmp = tmp.next;
    }
};
const printListRec = (list) => {

    console.log(list.value);

    if (list.next) {
        printListRec(list.next);
    }
};

const printReverseList = (list) => {
    let arr = [];
    let tmp = list;

    while (tmp) {
        arr.push(tmp.value);
        tmp = tmp.next;
    }

    for (var i = arr.length - 1; i >= 0; --i) {
        console.log(arr[i]);
    }
};
const printReverseListRec = (list) => {

    if (list.next) {
        printReverseListRec(list.next);
    }
    console.log(list.value);
};

console.log('pow: ' + pow(2, 3));
console.log('factorial: ', factorial(8));
console.log('sumTo: ', sumTo(100));
console.log('fib: ', fib(3));
console.log('printList: ', printList(list));
console.log('printListRec: ', printListRec(list2));
console.log('printReverseListRec: ', printReverseListRec(list));
console.log('printReverseList: ', printReverseList(list));

```
