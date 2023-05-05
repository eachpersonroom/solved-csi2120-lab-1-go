Download Link: https://assignmentchef.com/product/solved-csi2120-lab-1-go
<br>
This lab is based on the tutorial called <a href="https://tour.golang.org/list">A tour of Go</a> on golang.org. You are expected to work though the sections titled Basics and then solve the problems below. You can directly use the on-line go interpreter, called the sandbox, to try your programs.

Exercise 1: Go Basics: Functions

Read the section on <a href="https://tour.golang.org/basics/1">Packages, variables, and functions</a>.

Write a function in Go that takes as input a float variable and returns two integer values. One integer value which is the floor of the float value and the second integer value which is the ceiling of the float value. Print the result to console.

Exercise 2: Go Basics: Looping

Read the section on <a href="https://tour.golang.org/flowcontrol/1">Flow control statements: for, if, else, switch and defer</a>.

A program should print a pattern as follows to the console:

x   xx  xxx xxxxxxxxx xxxx  xxx   xx    x

Add two loops to the following program. The first loop should increase the “x” in lineSymb until the number of “x” is equal to

lineWidth

. The second loop should reduce the number of “x” until only one “x” is left.

package main import “fmt” func main() {        lineWidth := 5        symb := “x”        lineSymb := symb        formatStr := fmt.Sprintf(“%%%ds
”, lineWidth)        fmt.Printf(formatStr, lineSymb)}

<h3>Exercise 3: Go Basics: Structs and Pointers</h3>

Read the section on <a href="https://tour.golang.org/moretypes/1">More types: structs, slices, and maps.</a>.

A Go program is to read a person (last and first name) from console (use an input array if using the sandbox) and assign an Id counting up. The program must use the structure Person.

type Person struct {        lastName  string        firstName string        iD        int}

The main function looks as follows:

func main() {        nextId := 101        for {               var (                       p   Person                       err error               )               nextId, err = inPerson(&amp;p, nextId)               if err != nil {                       fmt.Println(“Invalid entry … exiting”)                       break               }               printPerson(p)        }}

Supply the functions inPerson and printPerson.

<h3>Exercise 4: Maps</h3>

Create a map that uses a string representing a course code as key. The value in the map needs to be a structure with basic information about the course. The following main routine:

import “fmt”    // Define a suitable structure  func main() {        // Create a dynamic map m         // Add the courses CSI2120 and CSI2110 to the map                  for k, v := range m {               fmt.Printf(“Course Code: %s
”, k)               fmt.Printf(“Number of students: %d
”, v.NStudents)               fmt.Printf(“Professor: %s
”, v.Professor)               fmt.Printf(“Average: %f

”, v.Avg)        }}

must print:

Course Code: CSI2110Number of students: 186Professor: LangAverage: 79.500000 Course Code: CSI2120Number of students: 211Professor: MouraAverage: 81.000000

<h3>Exercise 5 and Quiz:</h3>

<em>Please hand-in the answer to this question as a single go file on Virtual Campus during your lab session but at the latest by Friday 6:00pm! Remember, your submission will only count if you have signed the lab attendance sheet.</em>

Change the program below to use a single factored const definition for the labels of the switch statement. Use a map literal to hold all strings that are printed. Use the const as key. (All integer and string literals in the function printStatus shown in red must be replaced in your solution.)

// status_print.gopackage main import (        &amp;quotfmt&amp;quot) func statusPrint(state int8) {        switch state {        case 0:               fmt.Printf(&amp;quotState is %s (%d)
&amp;quot, &amp;quotIdle&amp;quot, 0)        case 1:               fmt.Printf(&amp;quotState is %s (%d)
&amp;quot, &amp;quotStart&amp;quot, 1)        case 2:               fmt.Printf(&amp;quotState is %s (%d)
&amp;quot, &amp;quotForward&amp;quot, 2)        case 3:               fmt.Printf(&amp;quotState is %s (%d)
&amp;quot, &amp;quotFast&amp;quot, 3)        case -1:               fmt.Printf(&amp;quotState is %s (%d)
&amp;quot, &amp;quotReverse&amp;quot, -1)        default:               fmt.Printf(&amp;quotInvalid state: %d
&amp;quot, state)        }        return} func main() {        var i int8        for i = -1; i &lt; 5; i++ {               statusPrint(i)        }}


