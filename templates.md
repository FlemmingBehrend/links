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

spec > Creates a skeleton jasmine test
```javascript
(function() {
    'use strict';

    describe('$DESCRIPTION$', function() {
        
        var cut, scope;
        
        beforeEach(module('$MODULE$'));
        
        beforeEach(inject(function ($rootScope) {
            scope = $rootScope;
        }));
        
        describe('initialization', function() {
        
            $END$
        
        });
    
    });

})();
```

dsr > Describe block
```javascript
describe('$DESCRIPTION$', function() {
    $END$
});
```

itsh > it should statement
```javascript
it('$DESCRIPTION$', function() {
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
public void $NAME$() {
    $END$
}
```
