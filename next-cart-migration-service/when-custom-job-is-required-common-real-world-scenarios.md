# When Custom Job Is Required: Common Scenarios

Most migration anxiety comes from one question: “Will my store work the same way after the move?”

For many stores, standard mapping is enough to transfer core entities cleanly. But some projects require more than transfer. They require preserving meaning and behavior when platforms represent data differently, or when business-critical information lives outside the standard platform model.

That is where **Custom Jobs** come in. In Next-Cart’s service model, Custom Jobs are delivered through **Custom Migration** (which is Managed Migration plus a Custom Job package) when standard mapping cannot reliably preserve the outcome you need.

### What is Custom Job

A Custom Job is not a generic add-on. It is targeted custom handling used when one of these is true:

* The data exists, but the target platform cannot represent it the same way by default
* The data is stored in a third-party system, plugin, or custom fields rather than native entities
* The data must be transformed to preserve meaning, behavior, or customer experience

A helpful mental model is this: standard migration moves what the platforms already agree on. Custom Jobs address what they do not.

If you are still deciding which service level fits your project, **\[How to Choose Next-Cart Migration Service Model]** provides a clean decision framework based on complexity, internal capacity, and risk ownership.

### Common scenarios that require Custom Jobs

#### **Scenario 1: Your store depends on third-party or custom data**

One of the most common sources of late surprises is discovering that a key feature is powered by app-driven data rather than native platform data.

Examples include:

* review systems that live in an app instead of the platform’s native product model
* custom fields created by plugins and used to drive storefront behavior
* integrations that store order or customer metadata outside standard fields

When that data is business-critical, it needs explicit planning. If reviews are a conversion driver for your store, the Learning Center’s review continuity guidance shows why relationship planning matters and when custom handling becomes the safest path.

#### **Scenario 2: You need transformations to preserve meaning and behavior**

Some data can be migrated, but will not mean the same thing on the target platform without transformation logic.

This is common when:

* Fields appear similar but behave differently across platforms
* The target requires a different structure to produce the same storefront behavior
* Special rules must be applied so the result matches how customers expect to browse or purchase

**Next-Cart insight**: the warning sign is not that data is missing. It is that the data is present but behaves differently. That is why a Demo Migration is most valuable when you validate outcomes, not only data presence. If you want the fastest proof step, **\[Demo Migration: What It Proves and How to Read Results]** shows how to interpret results without over-focusing on totals.

#### **Scenario 3: Your product structure is complex or constrained by the target model**

Catalog complexity is a predictable driver of custom scope.

Custom handling becomes more likely when:

* Variant structures are deep or inconsistent across products
* Option sets vary widely rather than following a consistent pattern
* Variant-level behavior matters for purchasing (images, SKU logic, pricing logic)
* Your current structure conflicts with how the target platform expects products to be modeled

If you are trying to size complexity realistically before deciding on service level, **\[Entity Points Explained: How Migration Scope Is Measured]** helps you estimate scope, while demo results help you confirm whether complexity is structural or simply “large”.

#### **Scenario 4: Teams involved require deeper proof than totals**

Many projects stall because teams cannot confidently approve readiness. Totals can look correct while structure is wrong.

You usually need Custom Jobs when approval depends on outcomes such as:

* A promotion exists and applies correctly, not merely that it was migrated
* Reviews appear on the correct products, not just “reviews exist”
* Important customer and order relationships remain usable for support and operations
* Category and navigation structure supports real shopping behavior

This is also where wording matters. Instead of “sign-off”, use “final approval” or “go-live approval”, because what teams actually need is confidence that business-critical workflows hold up under real use.

### What to do when you suspect custom scope

You do not need to guess, and you do not need to plan everything perfectly up front. You need early evidence and clear decisions.

A practical approach is:

* Define a short list of non-negotiable outcomes (what must remain true after launch)
* Identify where those outcomes are powered by apps, plugins, or custom fields
* Run a Demo Migration using your most complex products and representative orders
* review results with outcome-based validation, not only record counts

**Next-Cart insight**: Custom Jobs are most effective when they are used to preserve business-critical meaning, not to compensate for avoidable source data inconsistency. A demo often reveals which inconsistencies matter enough to clean up at the source versus which require custom handling to achieve the desired target behavior.

### Conclusion

Custom Jobs are typically required when standard migration cannot preserve meaning or behavior, especially when key data lives in third-party systems, needs transformation, or conflicts with target platform constraints. The goal is not to over-customize. The goal is to protect the outcomes that make your store usable, trustworthy, and ready for launch.

If you want a clean way to confirm whether your store needs Custom Migration, a Demo Migration that includes your most complex products and highest-risk behaviors is the fastest proof point. For stores with custom data behavior or SEO-sensitive launches, an assisted demo can be even more useful because it gives you a structured interpretation of what is truly at risk and what can remain standard.

If you want to align quickly on scope, risks, and the right service model without forcing a decision too early, Live Chat is the simplest way to get expert guidance and turn uncertainty into a clear plan.

#### FAQs

<details>

<summary><strong>What is the difference between Custom Jobs and Managed Migration?</strong></summary>

Managed Migration is expert-led execution of a standard migration flow. Custom Jobs are used when non-standard requirements require custom handling to preserve meaning or behavior, and they are delivered through Custom Migration.

</details>

<details>

<summary><strong>Does needing Custom Jobs mean my data cannot be migrated otherwise?</strong></summary>

Not necessarily. Many stores can migrate core data, but custom scope is about whether the result will behave correctly and match the outcomes you require. Custom handling is used when standard mapping cannot reliably reach that outcome.

</details>

<details>

<summary><strong>What is the most common cause of “surprise” custom scope?</strong></summary>

App-driven or custom-field data discovered late. Teams often assume a feature is native because it looks native in the storefront, then learn it is powered by a third-party system that requires special planning.

</details>

<details>

<summary><strong>How can I tell early if I will need Custom Jobs?</strong></summary>

Use a Demo Migration with a deliberately complex sample: best sellers, variant-heavy products, high-traffic categories, and representative orders.

Validate behavior, not only totals. If the outcome depends on data outside standard entities or requires transformation logic, custom handling becomes likely.

</details>

<details>

<summary><strong>Can Custom Jobs fix messy source data automatically?</strong></summary>

Some issues can be handled through mapping decisions or custom handling, but the best outcomes usually come from fixing inconsistent patterns at the source when possible.

Custom Jobs are most valuable when they preserve business-critical meaning, not when they replace basic cleanup.

</details>

<details>

<summary><strong>Should I decide on Custom Migration before testing a demo?</strong></summary>

Usually no. If you are uncertain, a demo-first approach is safer. Demo results often reveal whether your project behaves like a standard case, needs higher-touch guidance, or requires custom handling to reach the outcomes you care about.

</details>
