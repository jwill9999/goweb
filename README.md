# The Goweb project
A series of projects showing you how to serve a webpage to the browser and serve an API


# Go modules

## Explanation 

As a web developer, you may come across the term "Go module" when working with the Go programming language. A Go module refers to a self-contained unit of code that encapsulates a specific functionality or a set of related functionalities in a Go project.

In the context of Go, a module is essentially a collection of Go packages that are versioned together. It helps manage dependencies and facilitates code reusability across projects. Modules provide a structured and scalable approach to organizing and sharing code in the Go ecosystem.

Here are some key points to understand about Go modules:

1. Dependency Management: Go modules address the challenges of dependency management in Go projects. Each module has a go.mod file, which serves as a manifest or configuration file. It specifies the module's name, version, and its dependencies on other modules.

2. Versioning: Go modules follow the semantic versioning scheme (e.g., MAJOR.MINOR.PATCH) to manage versions of the module. This allows developers to express compatibility constraints and easily update dependencies when necessary.

3. Module Naming: Go module names are typically based on the version control system (VCS) hosting the code. For example, a module hosted on GitHub might have a name like "github.com/username/module-name." This convention ensures uniqueness and helps with package discovery.

4. Version Resolution: Go modules utilize a version resolution algorithm to determine the appropriate versions of dependencies when building a project. This process ensures that compatible versions are used, considering constraints specified in the go.mod file.

5. Module Cache: Go modules are cached on your development machine to improve build times and minimize network requests. The cache stores downloaded module versions, allowing you to work offline or avoid redownloading the same dependencies repeatedly.

6. Go Proxy: Go modules rely on Go Proxy servers to provide a central repository for downloading and hosting modules. By default, Go uses the proxy provided by proxy.golang.org, but you can configure your project to use an alternative proxy if desired.

Using Go modules offers several benefits, including simplified dependency management, reproducible builds, and better collaboration with other developers. It encourages code modularity and enables developers to create reusable components and libraries.

To start using Go modules, you can initialize a new Go module within your project directory by running the command `go mod init <module-name>`. This will create a go.mod file and allow you to manage dependencies effectively.

Overall, Go modules are a crucial part of the Go ecosystem, providing a robust mechanism for organizing, versioning, and sharing Go code across different projects.

> What command do I use to create a module?

1. go mod init name_of_module

This should be unique, e.g github.com/myGithubName/myGithubProject

## Output of `go mod init`
go: creating new go.mod: module github.com/test/goweb


## Some common `go mod` commands

- `go mod init`: initialize a new module
- `go mod tidy`: add any missing module requirements and remove unused ones
- `go mod vendor`: create a vendor directory containing the module dependencies
- `go list -m all`: list all direct and indirect dependencies of the current module
- `go get`: add a new dependency to the module and download it
- `go mod download`: download modules required by the module's go.mod file
- `go mod edit`: edit the module's go.mod file
- `go mod verify`: verify that the dependencies of the module are satisfiable
- `go mod why`: explain why a particular module requirement is needed.