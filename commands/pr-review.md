# PR Review

PR Link/Number: $ARGUMENTS

Instructions: Execute each task in the order given to conduct a thorough code review. Update GitHub with this review.

## Task 1: Product Management Review

Objective: Assess from a product management perspective:

- **Business Value**: Does this PR brings value to end users? In which way?
- **Solution**: Does the implementation solve the stated problem (if any)?
- **Exhaustiveness**: Does the logic handles the full user journey, not just the happy path?
- **Comformity to Industry Standards**:
  - Does this PR make sense from a business logic point of view?
  - Which aspects are common in the industry that this PR does not handle, if any?
  - Which aspects of the industry aren't handled now and will need to be handled in the future?

Action: Provide clear directives on how to ensure maximum user and business impact.

## Task 2: Implementation Manager Review

Objective: Assess customer deployment and technical integration impact.

- **Deployment Complexity**:
  - How does this affect customer implementation timelines and processes?
  - Does this PR makes it harder or easier for Implementation Managers to setup that feature (if feature requires setup)?
- **Migration Path**: Are there breaking changes requiring customer action? Plan migration strategy now if required
- **Integration Impact**: How does this affect existing customer?
- **Technical Documentation**: Is this feature customer-facing enough that it would require a setup guide?
- **Compatiblity**: ⚠️ Under which conditions does this feature work? Very often, we build something very bespoke to a specific customer with a specific setting/configuration.
  Then months later, we enable it for another customer with a similar setup however, slightly different, introducing major bugs.

## Task 3: Customer Success Review

- **Customer Communication**: What proactive messaging is needed if any?
- **Support Preparedness**: What new support scenarios need immediate preparation? Does this feature require the support team to know about it?
- **Value Messaging**: How do we communicate the customer benefit clearly?

## Task 4: Developer Review

Obective: Evaluate the code throughly from a senior engineer perspective:

- **Code Quality & Maintainability**: Is the code structured for readability and easy maintenance? If not, refactor now.
- **Performance & Scalability**: Will these changes operate efficiently at scale? If not, optimize immediately.
- **Future Proof**: Are there any trade-off being made in this PR? Whih one? What should our future-selves be aware of due to these trades-off?

Action: Leave a concise yet complete review comment, ensuring all improvements happen immediately—no deferrals.

## Task 5: Quality Engineer Review

Objective: Verify the overall quality, testing strategy and reliability of the solution:

- **Test Coverage**: Are there sufficient tests? Do the tests cover the most critical aspect of the PR's business logic?
- **Potential Bugs & Edge Cases**: Which edge cases have not been considered, if any?
- **Regression Risk**: Confirm that changes don't undermine existing functionality.

Action: Provide a detailed QA assessment.

## Task 6: Security Engineer Review

Objective: Ensure robust security practices and compliance:

- **Vulnerabilities**: Could these changes introduce security vulnerabilities?
- **Data Handling**: Are we properly protecting sensitive data (e.g. encryption, etc.)?
- **Compliance**: Compliance: Confirm alignment with any relevant security or privacy standards (e.g., OWASP, GDPR, HIPAA). Implement missing requirements immediately.

Action: Provide a security assessment.

## Task 7: UI/UX Design Review

Objective: Ensure optimal user-centric design

- **Visual Consistency**: Confirm adherance to brand/design guidelines. If not, adjust now.
- **Usability & Accessibility**: Validate that the UI is intuitie and compliant with accessibility standards.
- **Interaction Flow**: Assess whether the user flow is seamless. If friction exists, refine now.

Action: Provide a detailed UI/UX evaluation. Any enhancements typically set for “later” must be done immediately.

End of PR Review