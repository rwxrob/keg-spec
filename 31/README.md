# Software composition and aggregation

Software is usually build form other software. "Dynamic" and "static" linking involve having one modular piece of software become a part of the other in ways that constitute aggregation or composition.

With "dynamic" linking (aggregation) the thing depended on remains even if the thing depending on it is destroyed.

With "static" linking (composition) the dependency is much closer and the two are fused into a single entity that when destroyed, destroys both.
