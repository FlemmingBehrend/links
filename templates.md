# Javascript

cl > Console log statement
```javascript
console.log('$END$');
```

iife > Creates an immediately Invoked function expression
```javascript
(function() {
    'use strict';
    
    $END$

})();
```

us > Inserts 'use strict' statement
```javascript
'use strict';
$END$
```

vm > 'this' reference to the scope on a controller
```javascript
/*jshint validthis: true*/
var $VAR$ = this;
```

# Jasmine

dsr > Describe block
```javascript
describe("$DESCRIPTION$", function() {
    $END$
});
```

itsh > it should statement
```javascript
it("$DESCRIPTION$", function() {
    $END$
});
```

# Java unit tests

after > creates an after method
```java
@org.junit.After
public void after() {
    $END$   
}
```

itest > Integration test block for JUnit
```java
@org.junit.Test
@org.junit.experimental.categories.Category(dk.topdanmark.tr.test.IntegrationTest.class)
public void $NAME$() {
    $END$
} 
```

not > Creates a default nothing test method
```java
@org.junit.Test
@org.junit.experimental.categories.Category(dk.topdanmark.tr.test.UnitTest.class)
public void nothing() {
    assertTrue(true);
}
```

setup > creates @before method
```java
@org.junit.Before
public void setup() {
    $END$   
}
```

sub > creates a sub context
```java
public class $SUBCONTEXT$ {

    $END$
    
}
```

test > test block for JUnit
```java
@org.junit.Test
@org.junit.experimental.categories.Category(dk.topdanmark.tr.test.UnitTest.class)
public void $NAME$() {
    $END$
}
```
