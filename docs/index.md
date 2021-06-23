## AWS Step Function

**Introduction**

1. What is Step Function?
    - AWS Step Function is a serverless orchestration service that allows integrating multiple AWS services to collate & design an enterprise-critical application or workflow with advance conditional branching and error handling
    
    - Step Functions provides sequencing, error handling, retry logic, state, and offers a visualization-driven method to organize and represent the series of event-driven steps of your application through its graphical console.

    - And makes it easier and simpler to build and execute multiple-state event-driven critical applications. Step Functions can be invoked automatically via events or via APIGateway and simplifies tracking each step, and retries in case of errors, so the application executes in a defined sequence.

2. What is Amazon State Language (ASL)?

    - ASL is a JSON-based, structured language leveraged to design the state machine, a collection of states, that can do work (Task states), determine which states to transition to next (Choice states), stop execution with an error (Fail states), and so on.
    
    - ASL consist of three things 
      
      - State Machine Structure
      
      - Intrinsic functions
      
      - Common State Fields 
    
    - State Machine Structure: State machines are declared using JSON text and represents a structure consists of the following fields
      
      - Comment: description of state machine
      
      - StartAt: specify the state name from where the state machine to start the execution, and it is case sensitive 
      
      - TimeoutSeconds: maximum time in seconds a state machine can execute
      
      - Version: specify the version of ASL (default 1.0)
      
      - States: a comma-delimited set of states
      
        **Note**: From the above fields Comment, TimeoutSeconds, Version are optional fields
    
    - Intrinsic functions: Intrinsics are constructs like in programming languages, and can be leveraged to manipulate the data going to and from Task Resources
      
      - States.Format: string construction from literal and interpolated values, and takes one or more arguments
      
      - States.StringToJson: input is a single argument, a reference path to an escaped JSON string 
      
      - States.JsonToString: input is a single argument, a reference path, and the interpreter returns a string which is a JSON text
      
      - States.Array: input is a zero or more argument, and the interpreter returns a JSON array containing the Values of the arguments, in the order provided
          
    - Common State Fields
      
      - Type: state's type
      
      - Next: name of the next state that is run when the current state finishes
      
      - End: name of the state that is run at the end
      
      - Comment: human-readable description of the state
      
      - InputPath: state's input to be passed to the state's task for processing
      
      - OutputPath: state's input to be passed to the state's output 
      
        **Note**: From the above fields Comment, InputPath, OutputPath are optional fields

3. What is Workflow Studio?

    - Workflow Studio for AWS Step Functions is a visual workflow designer to create serverless workflows by orchestrating AWS services. 
    
    - With easy drag and drop capability you can design, edit, control how input and output is filtered or transformed for each state and configure error handling. It not helps to create a workflow but also validates the ASL and auto-generates code. 
    
    - Retrieved code can be reviewed, extracted for local development or AWS CloudFormation. Once finished, we can save the workflow, run it, and observe the outcome
