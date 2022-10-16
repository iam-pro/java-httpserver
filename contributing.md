# Contributing guidelines

## Before contributing

Welcome to [iam-pro/java-httpserver](https://github.com/iam-pro/java-httpserver)! Before sending your pull requests, make sure that you __read the whole guidelines__.

## Contributing

### Contributor

We are very happy that you consider implementing java http server for others! This repository is referenced and used by learners from all over the globe. Being one of our contributors, you agree and confirm that:

- You did your work - no plagiarism allowed
  - Any plagiarized work will not be merged.
- Your work will be distributed under [MIT License](LICENSE.md) once your pull request is merged
- Your submitted work fulfils or mostly fulfils our styles and standards    

__New implementation__ is welcome! For example, new solutions for a problem, different representations for a java http server designs with different complexity but __identical implementation__ of an existing implementation is not allowed. Please check whether the solution is already implemented or not before submitting your pull request.

__Improving comments__ and __writing proper tests__ are also highly welcome.

### Contribution

We appreciate any contribution, from fixing a grammar mistake in a comment to implementing java http server. Please read this section if you are contributing your work.

Your contribution will be tested by our [automated testing on GitHub Actions](https://github.com/iam-pro/java-httpserver/actions) to save time and mental energy.  After you have submitted your pull request, you should see the GitHub Actions tests start to run at the bottom of your submission page.  If those tests fail, then click on the ___details___ button try to read through the GitHub Actions output to understand the failure.  If you do not understand, please leave a comment on your submission page and a community member will try to help.

Please help us keep our issue list small by adding fixes: #{$ISSUE_NO} to the commit message of pull requests that resolve open issues. GitHub will use this tag to auto-close the issue when the PR is merged.

### HttpServer

A HttpServer is bound to an IP address and port number and listens for incoming TCP connections from clients on this address. The sub-class HttpsServer implements a server which handles HTTPS requests.

One or more HttpHandler objects must be associated with a server in order to process requests. Each such HttpHandler is registered with a root URI path which represents the location of the application or service on this server. The mapping of a handler to a HttpServer is encapsulated by a HttpContext object. HttpContexts are created by calling createContext(String,HttpHandler). Any request for which no handler can be found is rejected with a 404 response. Management of threads can be done external to this object by providing a Executor object. If none is provided a default implementation is used.

