# Entity Points Explained: How Migration Scope Is Measured

Migration pricing can feel confusing because raw counts can be misleading. Two stores might have the same number of products, but require very different effort and risk once you factor in order history, customer volume, and how much connected data must remain consistent after the move.

Entity Points are Next-Cart’s standardized way to measure migration scope and estimate plan size using weighted counts across the four core data types that drive most migration workload: Products, Customers, Orders, and Blog Posts.

### What are Entity Points?

**Entity Points** are a weighted method of measuring migration scope based on four core data types that drive most migration workload:

* Products
* Orders
* Blog posts
* Customers

Instead of treating every record as equal, Entity Points apply different weights to reflect real-world complexity.

Supporting data may still be included in scope depending on platform support, but it does not increase the Entity Points calculation.

### How Entity Points are calculated

Each core entity type has a coefficient:

* Products: **1.0**
* Customers: **0.5**
* Orders: **0.8**
* Blog posts: **0.6**

{% code overflow="wrap" fullWidth="false" %}
```
Entity Points = (Products × 1.0) + (Customers × 0.5) + (Orders × 0.8) + (Blog Posts × 0.6)
```
{% endcode %}

### Next-Cart Migration Service Package

A Next-Cart Migration Plan will includes

* The migration service model (Standard Migration, Managed Migration, or Custom Migration)
* The Entity Points Plan
* Custom Jobs (optional, depend on the customers' need)

A Migration Plan is valid for a one-year license period from the date of purchase. During the license period, the plan authorizes migrations as long as total Entity Points consumption stays within the purchased Entity Points Plan.

The Migration Plan applies to all migration types:

* Full Migration
* Recent Data Migration
* Re-migration

Your Migration Plan only apply to a specific migration direction:

**Source → Target**

For example, a plan purchased for **Shopify → WooCommerce** applies only to that direction. It cannot be reused for **WooCommerce → Shopify** or for a different target platform.

### Migration order and Entity Points consumption rules

Data is processed in a strict sequence:

1. Product
2. Customer
3. Order
4. Blog

Within each data type, records are migrated from oldest to newest.

Entity Points are consumed only when new data is migrated for the first time. Data that has already been successfully migrated is recorded in the migration system with a unique identification code for each record and can be re-migrated multiple times without consuming additional Entity Points.

If the Entity Points Plan is exhausted before all data is migrated, the remaining data will not be moved until the plan is upgraded.

#### Example: sequential migration and plan exhaustion

Assume a store has:

* 500 Products
* 100 Customers
* 600 Orders
* 100 Blog Posts

Entity Points: (500 × 1.0) + (100 × 0.5) + (600 × 0.8) + (100 × 0.6)\
\= 500 + 50 + 480 + 60\
\= 1,090 Entity Points

If the customer purchases a 1,000 Entity Points plan, the migration proceeds like this:

1. **Products migrate first**\
   **Consumption**: 500 × 1.0 = 500 Entity Points\
   **Remaining balance**: 1,000 − 500 = 500
2. **Customers migrate next**\
   **Consumption**: 100 × 0.5 = 50 Entity Points\
   **Remaining balance**: 500 − 50 = 450
3. **Orders migrate next**\
   Orders require 600 × 0.8 = 480 Entity Points, but only 450 remain.\
   The system migrates the portion that fits: approximately 450 ÷ 0.8 = 562 Orders, then stops.\
   **Remaining balance**: 0

At this point the customer can either keep the migrated results as-is or upgrade the Entity Points Plan to continue migrating the remaining data.

#### Re-migration of already migrated data

All successfully migrated records are labeled with a unique identification code for each record in the system. That recorded data can be re-migrated multiple times without consuming additional Entity Points.

Using the example above, the migrated set (500 Products, 100 Customers, 562 Orders) can be re-migrated again without consuming additional Entity Points, because those records were already processed and recorded as migrated.

#### Migrating new data after an initial migration

Entity Points are consumed only when the customer migrates new data that has not yet been recorded as migrated.

For example, after upgrading and completing the migration, assume the customer has consumed 1,090 Entity Points and has 910 remaining on a 2,000 plan. If the store later adds 120 new Products and 30 new Customers, migrating that new data consumes:

(120 × 1.0) + (30 × 0.5) = 120 + 15 = 135 Entity Points

**New total consumed**: 1,225\
**Remaining balance**: 775

### Migration Plan expiration and renewal

A Migration Plan is valid for one year from the date of purchase. If the plan expires, customers can renew to ensure continued access to the migration service.

Renewal requires payment for:

* The migration service model (Standard, Managed, or Custom), and
* The Entity Points Plan included in the migration package

Custom Jobs are not included in the renewal payment requirement for the migration package.

#### Entity Points Plan upgrades

When you need more capacity, upgrading your Entity Points Plan is designed to be cost-effective and straightforward.

* **Cost Efficiency**

You only pay the difference between your current plan and the new, higher-capacity plan you wish to purchase. This ensures you are never double-charged for capacity you've already secured.

* **Immediate Capacity**

The new plan immediately covers any capacity deficit, ensuring you can continue migrating your remaining data without interruption. This is particularly useful when migration scope increases unexpectedly, allowing for a seamless continuation of your project.

#### Scalable Pricing for Extremely Large Migrations

Our pricing model is structured to scale predictably, even for the largest and most complex migration projects.

For very large migration runs that exceed the standard Entity Points tiers, the following supplementary pricing logic applies:

If a migration plan surpasses **1,024,000 Entity Points**, an additional fee of **$50** is charged for every extra **100,000 Entity Points**.

This ensures that high-volume enterprise migrations are supported with a clear, predefined, and granular pricing structure.

### Conclusion

Entity Points help you estimate scope using weighted counts, but the plan behavior is what protects real project outcomes. Data migrates in a fixed order, Entity Points are consumed only when new records are migrated for the first time, and already migrated records can be re-migrated without consuming additional Entity Points. This keeps migration planning predictable and prevents plan limits from being bypassed through repeated small runs.

If you want to confirm scope in a practical way, running a **Demo Migration** gives you an early view of how key entities map and what needs attention in validation. When the store is more complex or you want a clearer readout, you can also request an **assisted demo** by sharing a small sample dataset so the Next-Cart team can run the demo and provide a structured results summary.

If questions come up while you are sizing scope or deciding how much help you need, **Live Chat** is the fastest way to get guidance on plan fit and whether Standard Migration, Managed Migration, or Custom Migration is the right match.

#### FAQs

<details>

<summary><strong>Do images, categories, or reviews increase Entity Points?</strong></summary>

No. Entity Points are calculated from products, orders, blog posts, and customers only.

Supporting data may still be included in scope depending on platform support, but it does not increase the Entity Points calculation.

</details>

<details>

<summary><strong>What happens if my Entity Points Plan runs out mid-migration?</strong></summary>

Migration processes data in the order Product → Customer → Order → Blog, oldest to newest. If the plan runs out, the system migrates only what fits within the remaining balance and stops. You can keep the migrated results or upgrade the plan to continue.

</details>

<details>

<summary><strong>Can I upgrade my Entity Points Plan after purchase?</strong></summary>

Yes. Plan upgrades are designed to cover the remaining scope when your needs exceed the current plan. In most cases, upgrades are handled as a price difference between plans rather than repurchasing from scratch.

</details>

<details>

<summary><strong>Is Next-Cart pricing a subscription?</strong></summary>

Next-Cart is a one-off payment model for your migration project, not a recurring monthly subscription.

The migration service purchase is valid for 1-year license from the date of purchase

</details>
