# APIMigrator

convert code from one programming language to another and make it all better

## first ai prompt

I want to feed a php file into the application, have ai review the code, create a suite of unit tests for the code in typescript for node.js, create the source code in node.js, refactor the code using SOLID principles and industry best practices, ensure logging occurs, and make it more secure. can you help me make the ai prompts needed for all these steps. I want the outputted source code to developed as if a principal software engineer created the code.

### results

Analyze the following PHP code for functionality, structure, and potential issues. Provide a detailed explanation of what the code does, any identified inefficiencies, and areas for improvement. Include recommendations to enhance readability, maintainability, and scalability following SOLID principles and industry best practices.

Based on the functionality of the provided PHP code, generate a comprehensive suite of unit tests in TypeScript for a Node.js environment. Ensure the tests cover all critical scenarios, edge cases, and error handling. Use a professional, best-practices approach, as if authored by a principal software engineer. Assume the use of a popular testing framework like Jest.

Convert the provided PHP code to TypeScript for a Node.js environment. Follow SOLID principles and industry best practices to ensure high-quality code. The resulting code should include clear type annotations, modular design, and idiomatic TypeScript syntax. Structure the output as if a principal software engineer created it, with a focus on scalability, maintainability, and readability.

Refactor the following TypeScript code to adhere to SOLID principles and industry best practices. Focus on creating a modular, scalable, and maintainable structure. Ensure each class and function has a single responsibility, dependencies are injected appropriately, and interfaces are used effectively. Include a brief explanation of the improvements made.

Enhance the following TypeScript code by adding comprehensive logging using a popular Node.js logging library (e.g., Winston). The logs should capture key actions, errors, and critical points of execution to aid in debugging and monitoring. Use structured logging and include relevant context for each log entry. Ensure logging adheres to best practices and does not expose sensitive information.

Review the following TypeScript code for potential security vulnerabilities and improve its security posture. Ensure secure coding practices are applied, such as input validation, output encoding, avoiding hardcoded secrets, and protecting against common vulnerabilities like SQL injection, XSS, and CSRF. Use industry best practices to make the code resilient against attacks.

Review the following TypeScript code as if you are a principal software engineer. Ensure it adheres to industry best practices, follows a clean and professional code style, and is optimized for performance and maintainability. Provide any additional refinements to enhance quality, including comments and documentation.

## Prompt 2

Yes please design a python application that implements this workflow

## Prompt 3

can you change the code so it takes the input file and output directory as a command line argument

## Prompt 4

if no command line arguments are provided can you ouput a helpful set of instructions on how to properly use this app

## Prompt 5

I received this error "You tried to access openai.ChatCompletion, but this is no longer supported in openai>=1.0.0 - see the README at [https://github.com/openai/openai-python] for the API."
eventually had to manually fix this "response = client.chat.completions.create("

## Prompt 6

how do i make vscode terminal use the virtual environment by default in my project

## Prompt 7

Ran out of the free gpt-4o runs flipped over to Claude
"I am getting this "Error calling OpenAI API: 'ChatCompletion' object is not subscriptable""

## Prompt 8

i need to modify the code so that when the typescript_code step runs it creates a typescript file with just the code in it and then make the new .ts file available to the refactor, logging, security and final review steps

## Prompt 9

I also need the unit tests to be created in a separate file as well and i want the unit test and code file so they can be executed immediately any findings or conversation from the prompt should go into the text files

## Prompt 10

i am building an api migration tool to migrate old php legacy code, create unit tests, create modern typescript (nodejs) code, ensuring we refactor it using SOLID patterns. I need to modify the generate prompt section as i want to use the old php code to review it, feed that information into the unit test prompt, and then use the unit test output in the tyepscript_code section. Once i have the typescript code i want to use the new code file in the refactor, logging, security and final review steps

## Prompt 11

I think there is a flaw in the prompt logic "Error calling OpenAI API: Error code: 500 - {'error': {'message': 'Timed out generating response. Please try again with a shorter prompt or with max_tokens set to a lower value" it looks like we are building all the prompts at the start, but what we need to do is run the first steps of review, unit_tests, and typescript_code with the old php code

Once the tyepscript_code is generated, then we need to build the remaining steps with the output from the ai calls. for example once we have typescript code we should send that code into the prompt to refactor, take the output from refactor and use that in the logging, take the output of logging and use that for the security prompt, the security ouput goes into the final_review and output the updated typescript code file that we are building

## Prompt 12

we need to refactor the generate_prompts what if we created functions for each of the steps instead of using ifs and elif

## Example

python .\APIMigrator.py "E:\SourceCode\CHHJIT\hunkware-API\v1\accounts\addresses.get.php"  "E:\SourceCode\CHHJIT\Migration"
