# Shared Libraries

- A Shared Library in Jenkins is a way to centralize and reuse pipeline code across multiple Jenkins pipelines.  
- Instead of repeating the same Groovy code in every Jenkinsfile, you can keep that logic in a separate Git repository (or folder) and reference it.  
- This makes your pipelines modular, DRY (Don’t Repeat Yourself), and easier to maintain.

  # Why use Shared Libraries?

**🔹 Without Shared Library**  
Every Jenkinsfile repeats the same steps (build, test, deploy).

**🔹 With Shared Library**  
You write those steps once in a shared library, then call them from any Jenkinsfile like a function.

<img width="683" height="509" alt="image" src="https://github.com/user-attachments/assets/e50cfe3b-30bb-4e12-958c-8c54dbcee08b" />


In Jenkins, a shared library is a way to store commonly used code(reusable code), such as scripts or functions, that can be used by different 
Jenkins pipelines. 

Instead of writing the same code again and again in multiple pipelines, you can create a shared library and use it in all the pipelines
that need it. This can make your code more organized and easier to maintain. 

Think of it like a library of books, Instead of buying the same book over and over again, you can borrow it from the library whenever you need it.

## Advantages

- Standarization of Pipelines
- Reduce duplication of code
- Easy onboarding of new applications, projects or teams
- One place to fix issues with the shared or common code
- Code Maintainence 
- Reduce the risk of errors

![Screenshot 2023-05-02 at 9 47 24 PM](https://user-images.githubusercontent.com/43399466/235724851-90a5cad6-ac0d-428b-9944-93fffea55180.png)
