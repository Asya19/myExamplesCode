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



console.log(pow(2, 3));
console.log(factorial(8));
console.log(sumTo(100));
console.log(fib(3));
console.log(printList(list));
console.log(printListRec(list2));
``
