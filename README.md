# otox-creator.github.io

who am i?



---
// from https://www.youtube.com/watch?v=9EOtSysFI-s&list=PLfllocyHVgsRwLkTAhG0E-2QxCf-ozBkk&index=57
// on easy rust ..
use std::collections::BinaryHeap;
fn main() {
    struct MyBinaryHeap {
        my_heap: std::collections::BinaryHeap<i32>,
    }
    impl MyBinaryHeap {
        fn my_pop(&mut self) -> Option<i32> {
            let i: Option<i32>;
            i = self.my_heap.pop();
            if i.is_some() { // this was the most problematic line 
                return Some(i.unwrap() + 5);
            } else {
                return None;
            };
        }
        fn new() -> MyBinaryHeap {
            MyBinaryHeap {
                my_heap: BinaryHeap::new(),
            }
        }
    }
    let mut heap = BinaryHeap::new();
    heap.push(100);
    heap.push(10000);
    heap.push(-5);
    heap.push(-500);
    heap.push(57);
    while let Some(number) = heap.pop() {
        println!("{}", number);
    }

    println!("___");

    let mut heap2 = MyBinaryHeap::new();
    heap2.my_heap.push(312);
    heap2.my_heap.push(-5);
    heap2.my_heap.push(22);
    heap2.my_heap.push(11);
    heap2.my_heap.push(41);
    heap2.my_heap.push(151);
    heap2.my_heap.push(251);
    heap2.my_heap.push(351);
    heap2.my_heap.push(-51);
    heap2.my_heap.push(-5001);

    while let Some(number) = heap2.my_pop() {
        println!("{}", number);
    }
}
---  
