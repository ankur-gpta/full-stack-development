# Scale the front-end

1. Design System thinking simplify the communication and collaboration between the teams.
    * Reuse (Micro frontends and component sharing)
            - Global Elements like chat (aPI backed Microfrontend) could be made in docker
            - Composable UI
    * Automation (tooling and testing) 
           - Visual regression testing
    * Culture (collaboration and contribution)
           - [Federated Ownership](https://medium.com/eightshapes-llc/team-models-for-scaling-a-design-system-2cf9d03be6a0)

## Rewrite the code

* Inexperience
* Sometimes its fun.
* Better Solution available
* Technical Debt

## Resilient Architecture

* Organization of code. Modular or layered. source code dependencies must point inwards. Easier to isolate impact of changes.
* Be Conservative about code reuse -> Avoid coupling code that diverges over time.
* Enforce your boundaries -> Forbidden dependency tests allows you to test the structure of your application. 
       `dependency-cruiser` - it allows to preserve your architecture over time.
