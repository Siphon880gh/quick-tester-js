Quick Tester JS
================
Quick assertion testing and pass/fail reports for javascript. 
By Weng Fei Fung.

Instructions
--------------
- Evaluate statements with quickTester.assert(eval, "error message if failed")
- You can pause the browser if eval false with: if(quickTester.assert(eval, "error message if failed")) debugger;
- Report pass and fail numbers with quickTester.report();

Advanced Use
--------------
- You can add a callback when assertion fails. It'd be good for animations, etc. It is not ideal for checking variables around the assertion line because the scope is moved to inside quickTester.assert()
- To check the current scope when assertion fails, notice that quickTester.assert returns true if the assertion fails, so you can do:
   ```
   if( quickTester.assert(typeof randomChar === "string", "randomChar should be a string") ) debugger;
   ```
   Then you can check the variables in the current scope.