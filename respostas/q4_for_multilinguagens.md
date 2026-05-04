//C
int i, j, n = 100;
int sum = 0;

for (i = 0, j = 17; i < n; i++, j--) {
    sum += i * j + 3;
}

//PHP
<?php
$n = 100;
$sum = 0;

for ($i = 0, $j = 17; $i < $n; $i++, $j--) {
    $sum += $i * $j + 3;
}
?>

//RUBY
n = 100
j = 17
sum = 0

(0...n).each do |i|
  sum += i * j + 3
  j -= 1
end

//GO
package main

import "fmt"

func main() {
    n := 100
    sum := 0

    for i, j := 0, 17; i < n; i, j = i+1, j-1 {
        sum += i*j + 3
    }

    fmt.Println(sum)
}

//RUST
fn main() {
    let n = 100;
    let mut sum = 0;

    for (i, j) in (0..n).zip((0..n).map(|x| 17 - x)) {
        sum += i * j + 3;
    }

    println!("{}", sum);
}
