Here's a refined version of the **Semantic Seed Venture Studio Coding Standards V2.0**, reducing charts by 50% and transforming steps into structured prompts for an LLM.  

---

# **Semantic Seed Venture Studio Coding Standards V2.0**
## **Introduction**
These coding standards guide our XP-oriented development team in building secure applications for banking and compliance-based clients. The principles focus on **code quality, security, collaboration, and Behavior-Driven Development (BDD)**.

---

## **📋 Backlog Management**
We use **Shortcut** to manage our backlog, ensuring that all work follows a structured workflow.

### **LLM Prompts for Backlog Management**
**Prompt 1:**  
*"Given a backlog managed in Shortcut, define the optimal workflow for starting, working on, and completing a feature. Include steps for test-driven development (TDD) and branching strategy."*

**Prompt 2:**  
*"Explain the importance of creating a WIP commit before implementing a solution in TDD. How does it enforce best practices in backlog management?"*

**Prompt 3:**  
*"Given a set of development tasks, classify them as a bug, chore, or feature, and explain how each should be handled in a structured backlog workflow."*

### **Standard Workflow**
1. **Start the top unstarted story in the backlog**  
2. **Branch Naming Convention**:  
   - `feature/{id}` for new features  
   - `bug/{id}` for bug fixes  
   - `chore/{id}` for maintenance tasks  
3. **TDD Workflow**:  
   - Write failing tests (**WIP: Red Tests**)  
   - Implement code to make them pass (**WIP: Green Tests**)  
   - Refactor and commit (**Refactor complete**)  
4. **Pull Request Process**:  
   - Mark story **Finished**, create a **PR**, and trigger a build  
   - Review PRs and merge  
   - Mark story **Delivered**  
5. **PM Review**: Accept or reject the story.  

---

## **📖 Story Types & Estimation**
We classify work into **Features, Bugs, and Chores** with **point-based estimation**.

### **LLM Prompts for Story Estimation**
**Prompt 4:**  
*"Given a backlog item, determine its classification as a feature, bug, or chore. Explain the reasoning and appropriate workflow steps."*

**Prompt 5:**  
*"Estimate the complexity of a given user story based on the Fibonacci scale (0, 1, 2, 3, 5, 8). Justify your estimate with reasoning."*

### **Story Estimation Guidelines**
- **0️⃣ (Zero Points)**: Quick fixes (typos, minor UI tweaks).  
- **1️⃣ (One Point)**: Straightforward tasks where the solution is clear.  
- **2️⃣ (Two Points)**: Slightly more complex but well-defined tasks.  
- **3️⃣, 5️⃣, 8️⃣ (Higher Points)**: Large tasks—should be broken into smaller stories.  

---

## **🎨 Coding Style Guidelines**
We enforce a **consistent style** for readability and maintainability.

### **LLM Prompts for Code Consistency**
**Prompt 6:**  
*"Given a function with inconsistent naming conventions, rewrite it to follow best practices for the given programming language."*

**Prompt 7:**  
*"Reformat a given block of code to enforce indentation, line length, and proper commenting."*

### **Key Standards**
- **Naming Conventions**: Use **camelCase** (JavaScript, Python), **PascalCase** (classes).  
- **Code Formatting**: Use **4-space indentation**, keep lines under **80 characters**.  
- **Comments**: Write **meaningful** comments, avoid outdated ones.  

---

## **🧪 Testing Strategy (TDD/BDD)**
We implement **Test-Driven Development (TDD) and Behavior-Driven Development (BDD)**.

### **LLM Prompts for Testing**
**Prompt 8:**  
*"Given a function description, generate BDD-style unit tests using Mocha or Jest."*

**Prompt 9:**  
*"Write an integration test that verifies the interaction between two microservices in a backend system."*

### **Test Structure**
1. **Unit Tests** (BDD-style frameworks like Mocha, Jasmine)  
2. **Integration Tests** (Ensuring components work together)  
3. **Functional Tests** (API Testing)  
4. **Test Suites** (Separate **unit, integration, and functional tests**)  

**Example BDD Test (Jest/Mocha):**
```javascript
describe('Calculator', () => {
  describe('addition', () => {
    it('should correctly add two positive numbers', () => {
      expect(add(5, 7)).to.equal(12);
    });
  });
});
```

---

## **🔄 Continuous Integration & Deployment (CI/CD)**
We maintain **rapid development cycles** through automation.

### **LLM Prompts for CI/CD**
**Prompt 10:**  
*"Describe an automated CI/CD pipeline for a web application, including build, test, and deployment steps."*

**Prompt 11:**  
*"Identify common CI/CD pipeline failures and suggest resolutions."*

### **Key CI/CD Practices**
- **Continuous Integration**  
  - Regularly merge code to **main**  
  - Ensure all tests pass before merging  
- **Continuous Deployment**  
  - Automate deployment to staging & production  

---

## **🔧 Version Control (GitHub)**
Our workflow ensures **collaboration and code quality**.

### **LLM Prompts for GitHub Workflows**
**Prompt 12:**  
*"Given a set of Git commits, summarize them into an informative PR description."*

**Prompt 13:**  
*"Explain the benefits of WIP commits and why all work must be committed daily."*

### **Key GitHub Practices**
- **Feature Branches** for development  
- **Pull Requests** for code review  
- **WIP Commits** to track progress  
- **End-of-Day Commits** ensure continuity  

---

## **📌 Conclusion**
By following these standards and integrating **BDD & TDD**, we ensure secure, high-quality software. Regular feedback is encouraged to improve processes.

---
