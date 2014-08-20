Mocha Cheat Sheet
=========

## BDD Interface
#### `describe`
Groups the testcases. `describe` can be nested one inside other.  

    describe('Logical group', function(){
      describe('First inner logical group', function(){
        // Test case listing
      });
      describe('Second inner logical group', function(){
        // Test case listing
      });
    });

#### `it`
Defines a test case via a function.  
It takes syntax `it('description', fnCallback)`   

    it('<textual represntation of testcase>', function(){
      // The test code which throws error on failure
    })


If callback is not given, then the test case is marked as **pending** test case.

#### `done`
A callback method parameter to be called in case of async test case. 
This is passed to function of `it()`. 
Absence of done in param assumes the test case synchronous and the test ends on function return.
`done` also accept an error as argument.

	it("check async response", function(done) {
	    asyncCall(function () {
	        // Test code
	        done(); 
			// or done(err);
	    });
	});


Alternatively, a promise can be returned instead of calling `done()` function.

	it("check async response with promises", function() {
	    return callThatReturnPromise(function () {
	        // Test code
	    });
	});


#### `beforeEach`
Runs before every test-case

#### `before`
Runs before the test-suit

#### `after`
Runs after the test-suit

#### `afterEach`
Runs after every test-case


#### `only`
Executes only the corresponding test-case(given by `it`) / test-group(given by `describe`) from the whole suit. This feature is termed as 'Exclusivity' feature.

    describe.only('Test-Group', function() {
    ...
    })
    // OR
    it.only('Test-Case', function() {
    ...
    })

#### `skip`
Skips out the corresponding test-cases/test-groups. The skipped items go to pending state.

    describe.skip('Test-Group', function() {
    ...
    })
    // OR
    it.skip('Test-Case', function() {
    ...
    })

-----

#### `timeout`
Timeouts can be applied to entire suit or specific test-cases

	describe('Test-Suite', function(){
	  this.timeout(500);
	
	  it(Test-Case', function(done){
	    this.timeout(500);
	  });
	})

----
## TDD Interface

suite(), test(), setup(), and teardown().

	suite('Test-Suite', function(){
	  setup(function(){
	    // ...
	  });
	
	  suite('Test-Suite', function(){
	    test('Test-Case', function(){
	      // Test Code
	    });
	  });
	});


## Reporters

- `dot`: Dot-Matrix style
- `spec`: Hierarchical view nested just as the test cases are
- `nyan`
- `tap`
- `list`
- `json`
- `markdown `
- `html`

[More reporters](https://github.com/visionmedia/mocha/wiki#interfaces--reporters)