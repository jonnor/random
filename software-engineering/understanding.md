
# Making software-based systems more understandable

What does it mean?
How to improve upon current practices?

## Ways of contributing

* Furthering state-of-the-art
* Distilling best-practices
* Popularizing/spreading existing best-practices
* Tools that make best practices more accessible/effective

## Aspects of understanding

* Understanding the *domain*
* Understanding the problem
* Understanding the (current) solution

## Measuring understanding
What is current state?
Is B an improvement over A?
Does a hypotetical development C seem like it could be an improvement? 

Guidelines. To which degree can a system developer:

1) Predict what a given change will do to the behavior of the system?
2) Determine what change is needed to achieve desired behavior?

## Observing systems
Verifying our understanding of a system requires observing it.
Ensure that our mental models are in sync with reality.

For each test: Stimulate a condition, check what happened, evaluate it.

## Considerations

How many tests are performed? How often are they ran?
How much of the input domain does it cover? How widely and how densely? What are the gaps?
How long does test take to execute?

How easy to test permutations/variations/modifications of system?

How observable are (unexpected) in-field failure/anomalies? How easy to go to a reproducable case?

## Existing practices

Note: Many of these practices come from the perspective of 'verification',
and assumes that the desired system behavior is already defined (correctly).

Note: Automated testing practices usually applied more often
to (relatively small) sub-systems than entire systems.

### Manual testing
One-few tests.
Manual, ad-hoc observeration. 'looks good to me'
Manual structured testing. Make observation/measure, evaluate according to a set standard

### Unit-testing
Automated stimulation. Automated evaluation.
Strict pass/fail only. Often result evaluation stops at first failure.
One-few tests.
Reproducable across systems.

### Continious testing
Tests ran automatically instead of having to be triggered manually.
On changes checked into source-control, by a CI server.
On changes made while developing, on the developer system.

### Mainstream/fringe
As of 2017, above practices are quite mainstream, while the below are pretty fringe.

### Data-driven testing
Modification of unit-testing.
Tens of tests.
Tests still mostly manually specified by developer, may miss important cases.
Can make it easier to add regression

### Property-based-testing
Hundreds-thousands of tests.
Wide domain coverage. Random sampling means each run has gaps, but moving around.
Automatic synthesis of concrete cases, could potentially run all the time. Endurance testing.
Still strict pass/fail only.
Automatically reduces failing cases to minimal testcase.

Notes: https://github.com/jonnor/projects/tree/master/invariants-based-testing#property-based-testing

### Mutation-testing
Changes the system to induce errors. Most commonly used to 'test the tests'.

### Model checking
Given a mathematical/logic model of a system, check whether this model meets a given specification.
The model can be theoretically be checked exhaustively. In practice bounded.
Generates counterexample automatically for failing property.
Problem, the model is usually not the system. Sometimes system can be derived from model.

Standard in semicondutor manufacturing, very rare in software outside safety-critical domains.

## Limitations

Typically the only evaluation is Pass|Error.
No support for numerical or complex values.
Pass condition must be decided up-front. Changing it requires re-running tests.

Reporting is low-level, usually a text string rendered per testcase.
No tools for visualization of results.
Not enabling subjective evaluations of 'fitness'.

Storing test results in structured way is rare.

No standardized way executing tests against multiple versions of system.
No standard tools for comparing multiple results against eachother.

