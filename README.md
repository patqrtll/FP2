# Final Project Assignment 2: Explore One More! (FP2) 
DUE March 30, 2015 Monday (2015-03-30)
Patrick Quaratiello

```
#lang racket
(require pict)

(define upsidedown (text "This is upside down!" (cons 'italic 'roman) 12 (* 3 pi)))
(define frametext (frame (text "This is text inside a frame!" (cons 'italic 'roman) 12 (/ pi 2)) #:color "medium goldenrod" #:line-width 3))	
(define head (circle 80)) ;; head
(define eye (circle 15)) ;; eyes
(define ineye (colorize (circle 5) "blue"))  ;; inner eye
(define nose (colorize (filled-ellipse 40 30) "tomato")) ;; nose?
(define brim (colorize (filled-rectangle 80 10) "black")) ;; brim
(define top  (colorize (filled-rectangle 50 40) "black")) ;; top
(define face (ct-superimpose (rc-superimpose head (cbl-superimpose eye ineye)) (lc-superimpose head (cbl-superimpose eye ineye)) (cbl-superimpose head nose))) ;;face
(define facehat (vc-append  top (lt-superimpose brim face))) ;; face add hat
(vc-append  5 upsidedown (hc-append  10 frametext facehat)) ;; face with hat and some words around it

```

### My Library: pict
I messed around with modifications you can do with text, and then began to make some shapes and attempt to create something that resembles a face with a tophat. For the text I played around with the angles mostly and changed the frame around it. I used the superimpose and append to get the pieces to where they need to be and tried to add some colors to the shapes. I was trying to drive around with a different library for a while (the game board one), but I couldn't really get anything that was worth showing so I decided to try something different. I may go back to that library and have another go at it though. There should be a link to a picture of the output below, a face with a tophat and some text placed around him using the pict library.

Face with tophat and some text around him [here] (https://github.com/patqrtll/FP2/blob/master/Images/Pict_FP2.png).



