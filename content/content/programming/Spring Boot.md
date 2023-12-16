- Used to create Spring based applications in a faster way
- [Spring Initializr](https://start.spring.io/): used to create Spring Boot projects with preselected
	- Dependency manager
	- Version of spring boot
	- Dependencies
		- **Spring Web**: to create RESTful APIs
		- **Spring Security**: to create authentication and authorization methods
		- **DevTools**: LiveReload
	- Language
- Spring Boot can be used in Java, which is a *Oriented Object Programming* language, because of that, our code can be organized using:
	- Model
		- Used to define the structure of the data
		- Has attributes
	- Controller
	- Repository
- JWT Security API
	- Permissions
		- We use a `RoleEnum` and a `PermissionEnum` to define roles and permissions of each role in our application
		- We store In the `PermissionEnum` every permission available on the system
		- We define in the `RoleEnum` which permissions a Role has
		- Example:
		  ```java
		  MANAGER(
		          Set.of(
		              PermissionEnum.MANAGER_CREATE,
		              PermissionEnum.MANAGER_READ,
		              PermissionEnum.MANAGER_UPDATE,
		              PermissionEnum.MANAGER_DELETE
		          )
		  ),
		  ```