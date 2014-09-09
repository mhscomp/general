#MHS Robotics Club: Languages#

<b>Arduino</b><br/>
A mash-up of Java and C++, it is a simple language used for Arduino micro controllers.

<img src="http://www.robotshop.com/blog/en/files/arduino-mega-usb-microcontroller-board-B.jpg">

<b>Processing</b><br/>
Processing is very similar to Arduino, and they often interact.

<blockquote>
Initially created to serve as a software sketchbook and to teach computer programming fundamentals within a visual context, Processing evolved into a development tool for professionals. Today, there are tens of thousands of students, artists, designers, researchers, and hobbyists who use Processing for learning, prototyping, and production. (Processing's website)
</blockquote>

Processing is good for data visualization, but is difficult to integrate with other projects.

<b>Haskell</b><br/>
Haskell is a functional language that is used for higher-level programming while compilers handle the lower-level stuff.

For example, in Java, this creates a list of all even numbers up to 100, and another list omitting the first five of them:
```java
final int LIMIT = 50;
int[] a = new int[LIMIT]; //an array
int[] b = new int[LIMIT]; //another array
for(int i = 0; i < LIMIT; i++){
    a[i] = (i + 1) * 2;
    if(i >= 5){
        b[i - 5] = a[i];
    }
}
```

In Haskell:
```haskell
let a = [2,4..100]
let b = drop 5 a
```

Haskell is used for business analysis and enhancing existing code. It is difficult to learn and set up, however. It has won support for being easy to scale, and for minimizing errors, which has led to rise in popularity.

<b>Hack</b><br/>
Hack is made by Facebook, and is meant to integrate with PHP. It's goal is to add functions common in other languages to PHP, enhancing it. 

This includes types (such as integers or strings) and other tools found, for example, in Java.