# Cook - Recipe Manager

Cook is a simple example application that serves as a reference implementation for creating Go REST applications. It is designed to focus on microservices for CRUD operations on single resources, providing a clear example of a RESTful microservice implemented in an elegant and straightforward way.

## Key Features

- Versionable REST API: Cook enables the implementation of a versioned REST API, allowing for future updates and enhancements.
- Minimal Dependencies: The application strives to minimize external dependencies and primarily utilizes the Go standard library. However, alternative implementations may be considered if they offer better solutions for specific features. For example, we have chosen to use [Chi](https://github.com/go-chi/chi) as the routing library.
- Use of Interfaces: Cook leverages interfaces to facilitate testing and enable the plugging in of alternative implementations, promoting modularity and flexibility.
- Single Resource Focus: Cook is specifically designed for managing a single resource, but it can be extended as desired to accommodate more complex business rules, you can easily adapt the generated code from the code generator in another repository to suit your more complex use cases.

## Extensibility and Code Generation

Cook is designed as a reference application that focuses on managing a couple of , recipes in this case, and provides a starting point for building Go based services.

There will be a separate code generator repository that utilizes Cook as a foundation for creating simple RESTful microservices specifically tailored for managing an intrinsically related group of resources (list-item, recipe-ingredient-directions, course-students, etc). The [code generator](https://github.com/foorester/crud) will provide developers with the ability to quickly generate the basic structure and functionality and extended later if required.

While the generated code will be optimized for managing a small set of resources, developers will be not limited to this constraints and will be able to adapt and modify the generated code to suit their specific and more complex use cases.

## Usage

[To be completed]

## Notes
This projects utilizes a customized fork of the OpenAPI generator for its server and client interface needs. While the original version of the generator, available at https://github.com/deepmap/oapi-codegen, remains a viable option, we have opted to use [this forked version](https://github.com/foorester/oapi-codegen) for improved code clarity.

One concrete example highlighting is the transformation of a server interface function originally named `DeleteRecipeBooksBookIdRecipesRecipeIdIngredientsIngredientId` into `DeleteIngredient`.

## License

This project is licensed under the MIT License. Feel free to use and modify it as per the terms of the license.
