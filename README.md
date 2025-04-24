# CS 230 Portfolio Submission: The Gaming Room Project  

## Client Summary 
The Gaming Room sought to expand their Android-exclusive game *Draw It or Lose It* into a cross-platform solution (Windows, macOS, Linux, and mobile). As a creative guessing game requiring unique team/player names and single-instance memory constraints, the project demanded a robust architecture balancing scalability, security, and real-time multiplayer functionality. My software design document outlined a Linux-based server solution with PostgreSQL storage, RESTful/WebSocket APIs, and containerized deployment to meet these needs.

## Strengths of the Documentation 
I excelled in:  
- Architectural Clarity: Clearly justified Linux over alternatives (cost, scalability) with specific kernel optimizations.  
- Technical Precision: Detailed memory/storage management techniques (e.g., PostgreSQL MVCC, Linux OOM killer).  
- User-Centric Design: Translated "unique names" and "single instance" requirements into Singleton/Iterator patterns.  

## Design Document Process Benefits  
Working through the document helped:  
- Preempt Challenges: Identifying distributed systems pitfalls early (e.g., session persistence during outages).  
- Align Stakeholders: Visualizing the UML class diagram ensured developer/client consensus on data relationships.  
- Streamline Coding: Predefined patterns (like object pooling) reduced refactoring during implementation.  

## Areas for Revision  
I would enhance the Evaluation section by:  
- Adding quantitative comparisons (e.g., Linux vs. Windows Server throughput benchmarks).  
- Including mock-ups of the client-facing API documentation.  
- Expanding the security section with a threat matrix (DREAD model).  

## User Needs Interpretation  
The client’s requirements were distilled into:  
1. Technical Constraints: Singleton pattern enforced single game instances; Iterator validated unique names.  
2. Experience Goals: WebSocket integration enabled real-time drawing synchronization for multiplayer immersion.  
3. Business Needs: Cross-platform support drove the containerized Linux/Python stack choice.  

Considering user needs ensured the design solved actual problems rather than hypothetical edge cases. 

## Future Design Strategies  
For similar projects, I would:  
- Prototype Early: Build a minimal WebSocket demo to validate latency thresholds.  
- Leverage Diagrams: Use sequence diagrams alongside UML to model API workflows.  
- Conduct User Stories: Formalize requirements gathering with stakeholder interviews.  
