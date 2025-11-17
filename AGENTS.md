# AGENTS.md

## Repository Overview
This repository contains an AngularJS seed application demonstrating REST API consumption. It's based on the tutorial published at http://coder1.com/articles/consuming-rest-services-angularjs.

## Recent Changes

### August 7, 2013
**Initial Project Setup** (Commit: 6fcad6c)
- Set up complete AngularJS seed project with REST API integration
- Fixed variable name in partial1.html template
- Integrated with GitHub Issues API for demonstration purposes

## Key Components

### Application Structure
- **app/**: Main application directory
  - **js/**: JavaScript source files
    - `app.js`: Main application module configuration
    - `controllers.js`: Controller definitions (MyCtrl1, MyCtrl3)
    - `services.js`: Service layer with AngularIssues factory
    - `directives.js`: Custom directives
    - `filters.js`: Custom filters
  - **partials/**: View templates
    - `partial1.html`: GitHub Issues list and detail view
    - `partial2.html`: Secondary view
  - **css/**: Stylesheets
  - **lib/**: Third-party libraries (AngularJS modules)

### Features Implemented

#### REST Service Integration
- **AngularIssues Service**: $resource-based service for GitHub API
  - Endpoint: `https://api.github.com/repos/angular/angular.js/issues/:number`
  - Custom action: `getIssue` for fetching individual issues
  - Standard CRUD operations available

#### Controller Features (MyCtrl1)
- **Issue List Management**:
  - State filtering (open/closed issues)
  - Sorting by created date with direction toggle
  - Issue detail view navigation
  - Client-side text filtering
- **Data Model**: Centralized scope data using `myData` object (best practice)
- **API Integration**: Asynchronous data loading with callbacks

### Testing Infrastructure
- **Unit Tests**: Karma configuration for unit testing
  - Specs for controllers, directives, filters, and services
  - Located in `test/unit/`
- **E2E Tests**: End-to-end testing with Angular scenario runner
  - Configuration in `config/karma-e2e.conf.js`
  - Test scenarios in `test/e2e/scenarios.js`

### Development Tools
- **Scripts**:
  - `web-server.js`: Development server
  - `test.sh`/`test.bat`: Unit test runners
  - `e2e-test.sh`/`e2e-test.bat`: E2E test runners
  - `watchr.rb`: File watcher for continuous testing
- **CI/CD**: Travis CI configuration included

## Modified Files in Original Tutorial
According to README.md, the following files demonstrate the REST integration:
- `index.html`: Main application shell
- `js/services.js`: AngularIssues REST service
- `js/controllers.js`: MyCtrl1 with GitHub API integration
- `partials/partial1.html`: Issues list UI (Note: README mentions partial1.js, but actual file is .html)

## Angular Version
- Angular v1.x (version.txt in lib directories)
- Includes modules: cookies, loader, resource, sanitize
- Mock and scenario testing libraries included

## Architecture Notes
- Uses `ngResource` module for REST interactions
- Implements best practice of using a data object on $scope
- Demonstrates async callback patterns with $resource
- Includes commented examples of alternative $http approach

---

*Last Updated: 2025-11-17*  
*Based on commit: 6fcad6c (August 7, 2013)*
