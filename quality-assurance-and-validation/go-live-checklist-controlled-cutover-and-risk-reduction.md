# Go-live Checklist: Controlled Cutover and Risk Reduction

Go-live is not a single moment. It is a controlled cutover process designed to minimize risk to sales, customers, and traffic.

Most launch failures come from timing gaps:

* the new store is not fully aligned with recent orders and customer activity
* redirects are not ready when the domain switches
* operational settings are incomplete, causing payment or email disruptions

This checklist focuses on a controlled, low-surprise launch.

#### 1) Establish a cutover window and roles

**Checklist**:

* Define the planned cutover window and communication plan
* Assign owners for validation sign-off, redirects, payments, and customer support readiness
* Define escalation paths and a rollback decision owner

#### 2) Confirm pre-launch validation is signed off

**Checklist**:

* High-risk products validated (best sellers and complex products)
* Catalog navigation validated for critical browse paths
* Customer and order usability validated for representative scenarios
* Priority URL list validated for continuity expectations

#### 3) Confirm the final sync plan

If your source store remained active during build, you need a final alignment.

Use **Recent Data Migration** to sync recent changes to your target store before go-live.

**Checklist**:

* Confirm which data types must be up-to-date at launch (orders, customers, inventory, products)
* Confirm when the final sync occurs relative to cutover
* Confirm who signs off after the final sync completes

#### 4) Confirm redirect readiness for SEO continuity

**Checklist**:

* Priority old URLs are mapped to correct destinations
* Redirect logic is ready to function immediately after domain cutover
* You have a plan to add missing redirects quickly if gaps are found

#### 5) Confirm operational continuity settings

Even if migration data is correct, operations can break if basic settings are incomplete.

**Checklist**:

* Email settings on the new store are tested conceptually for order notifications
* Payment processing readiness is confirmed
* Tax and shipping behavior is reviewed for key scenarios
* Analytics and tracking are prepared so you can measure launch performance

#### 6) Make the domain change a planned step, not a scramble

**Checklist**:

* The domain cutover has a clear owner
* Timing is coordinated with the final sync
* Monitoring begins immediately after cutover

#### 7) Run a first-hour smoke test

**Checklist**:

* Place a test order end-to-end
* Confirm confirmation emails behave as expected
* Confirm key pages and checkout flow are usable
* Confirm redirect behavior for priority URLs

#### Conclusion

A controlled go-live reduces risk by aligning timing: validation sign-off, redirect readiness, final sync, and immediate monitoring.

**CTA:** If you want to reduce launch stress, plan your cutover around **Recent Data Migration** so your final sync is intentional, not rushed.

#### FAQs

<details>

<summary><strong>Should I stop making changes on the old store before launch?</strong></summary>

It's usually best to minimize last-minute modifications as the launch approaches, helping ensure a smoother transition. The most important thing is to plan the final synchronization and sign-off process carefully, so everyone is aligned and ready for a successful launch.

</details>

<details>

<summary><strong>What is the most common go-live mistake?</strong></summary>

It’s launching your system without verifying that redirects are fully functional and without a solid plan to synchronize recent orders and customer data, which can cause delays and confusion.

Carefully preparing these aspects ensures a smoother transition and a more successful launch.

</details>
