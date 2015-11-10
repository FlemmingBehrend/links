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

specc > Creates a skeleton jasmine test for a controller
```javascript
(function() {
    'use strict';

    describe('$DESCRIPTION$', function() {
        
        var cut, scope, ctrl;
        
        beforeEach(module('$MODULE$'));
        
        beforeEach(inject(function ($rootScope, $controller) {
            scope = $rootScope;
            ctrl = $controller;
        }));
        
        function createController() {
            cut = (function () {
                return ctrl('$CONTROLLER$', {
                    $scope: scope
                });
            })();
            return cut;
        }

        describe('initialization', function() {
        
            it('can initialize the controller', function() {
                cut = createController();
                expect(cut).toBeDefined();
            });

            $END$
        
        });
    
    });

})();
```

specs > Creates a skeleton jasmine test for a service
```javascript
(function() {
    'use strict';

    describe('$DESCRIPTION$', function() {

        var cut, httpBackend;

        beforeEach(module('$MODULE$'));

        beforeEach(inject(function ($SERVICE$, $httpBackend) {
            cut = $SERVICE$;
            httpBackend = $httpBackend;
        }));

        afterEach(function () {
            httpBackend.verifyNoOutstandingExpectation();
            httpBackend.verifyNoOutstandingRequest();
        });

        describe('initialization', function() {

            it('has initialized the class under test', function() {
                expect(cut).toBeDefined();
            });

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
