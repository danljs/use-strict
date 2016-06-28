# use strict

1. Using a variable, without declaring it, is not allowed:
```
"use strict";
x = 3.14; 
```

1. Using an object, without declaring it, is not allowed:
```
"use strict";
x = {p1:10, p2:20};
```

1. Deleting a variable (or object) is not allowed.
```
"use strict";
var x = 3.14;
delete x; 
```

1. Deleting a function is not allowed.
```
"use strict";
function x(p1, p2) {}; 
delete x; 
```

1. Duplicating a parameter name is not allowed:
```
"use strict";
function x(p1, p1) {};
```

1. Octal numeric literals are not allowed:
```
"use strict";
var x = 010; 
```

1. Escape characters are not allowed:
```
"use strict";
var x = \010; 
```

1. Writing to a read-only property is not allowed:
```
"use strict";
var obj = {};
Object.defineProperty(obj, "x", {value:0, writable:false});

obj.x = 3.14;
```

1. Writing to a get-only property is not allowed:
```
"use strict";
var obj = {get x() {return 0} };

obj.x = 3.14; 
```

1. Deleting an undeletable property is not allowed:
```
"use strict";
delete Object.prototype; 
```

1. The string "eval" cannot be used as a variable:
```
"use strict";
var eval = 3.14; 
```

1. The string "arguments" cannot be used as a variable:
```
"use strict";
var arguments = 3.14;  
```

1. The with statement is not allowed:
```
"use strict";
with (Math){x = cos(2)};
```

1. For security reasons, eval() is not allowed to create variables in the scope from which it was called:
```
"use strict";
eval ("var x = 2");
alert (x);               // This will cause an error
```

1. Future reserved keywords are not allowed in strict mode. These are:
	1. implements
	1. interface
	1. let
	1. package
	1. private
	1. protected
	1. public
	1. static
	1. yield
```
"use strict";
var public = 1500;
```
