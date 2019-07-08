# cmd-lang
Verbal command programming language

Example:

```bash
  newModule Test

  assign a add 1 2
  assign b subtract 7 3
  assign c multiply 2 3
  assign d divide 10 5
  
  assign Point newRecord
  addField Point x type int
  addField Point y type int

  macro SelfPointX dot self x
  macro SelfPointY dot self y
  macro OtherPointX dot other x
  macro OtherPointY dot other y
  macro NewPointX add SelfPointX OtherPointX
  macro NewPointY add SelfPointY OtherPointY
  macro AddPoint new Point x NewPointX y NewPointY
  macro ReturnAddPoint return AddPoint
  
  addMethod Point add
  addArgument Point add self
  addArgument Point add other
  addBody Point add ReturnAddPoint

  assignMacro ReturnSubPoint substitute ReturnAddPoint add sub

  addMethod Point sub
  addArgument Point sub self
  addArgument Point sub other
  addBody Point add ReturnAddPoint

  assign pointA new Point x 1 y 2
  assign pointB new Point x 3 y 4
  assign pointC add pointA pointB
```
