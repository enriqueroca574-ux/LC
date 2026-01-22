---
layout:
  width: default
  title:
    visible: true
  description:
    visible: true
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
  metadata:
    visible: true
---

# Square Data Model Differences in Migration

Square’s data model is designed to support unified commerce, so the target platform’s “shape” is often different from carts that were built ecommerce-first. In migration, this mostly shows up in how Square represents products and purchasable choices, how orders relate to payments, and how customer history is structured.

### The Square catalog model (what you are really migrating into)

Square describes its catalog as a set of objects that represent commerce concepts such as items, item variations, categories, modifiers, discounts, taxes, and more.

Even if you never use the API, this catalog structure influences how data behaves in Square Online and operations.

#### Items, options, and variations

Square supports creating item options to generate variations (for example: size, color), then using those variations as purchasable units. In migration terms, that means your “variant structure” is not only a data field, it is a buying-behavior contract. When variation logic changes, conversion can change.

**What to do with this insight:**

When planning a Demo Migration sample, include products with the highest variation complexity so you validate buying behavior first.

#### Modifiers and add-ons

Square’s catalog model includes modifier concepts (for add-ons and choices), which can behave differently than typical “variants”. If your source store uses add-ons, bundles, or product personalization driven by apps, treat that as higher risk until proven in a demo.

#### Inventory and channel sync

Square positions Square Online as connected to your Square catalog inventory, with quantities updating as customers purchase online. This unified approach is one reason many sellers choose Square as a target, but it also means you should validate inventory-relevant behaviors early.

#### Customer records and history

Square’s Customer Directory is built around maintaining customer profiles and history in a centralized way. Square Online also supports customer accounts for experiences like order tracking and reordering. In migration, the key question is not “did customers import,” but “does the target customer profile support support-team workflows and retention goals.”

#### Orders, totals, and payments

Square’s order and refund workflows are designed around transactions and tenders. In some scenarios, Square can treat monetary values and “paid” signals in ways that are surprising when orders were imported as historical records. This is why order-history expectations should be treated as a validation topic, not an assumption.

### How Next-Cart reduces model mismatch risk

Next-Cart’s validation mindset is built around relationships and behavior, not raw counts. This includes mapping product variation structure to preserve purchasable behavior and preserving customer-order linkage so history remains meaningful. The practical takeaway: validate how the store works in real workflows.

If you want the canonical framework for this approach, **\[Demo Migration: What It Proves and How to Read Results]** explains why demos should focus on representative complexity, not volume.

### Conclusion

Square’s model is designed to unify commerce, which can be a strong advantage after migration, but it also means “equivalent data” may not behave equivalently. The safest way to migrate into Square is to treat product options, modifiers, customer history, and order interpretation as the core behavior areas that must remain true.

Run a Demo Migration that includes complex products, meaningful category paths, and a few representative orders. If you prefer, you can request that Next-Cart run the Demo Migration using your sample data and share structured findings. If you are unsure whether your store requires Standard, Managed, or Custom, Live Chat is the fastest way to get an expert recommendation based on real evidence from your data.

### FAQs

<details>

<summary><strong>How does Square represent product variations?</strong></summary>

Square supports item options that generate variations (such as size or color), and those variations become purchasable units.

</details>

<details>

<summary><strong>What is Square’s Customer Directory?</strong></summary>

Square describes Customer Directory as a way to manage customer profiles and history centrally.

</details>

<details>

<summary><strong>Why do “data model differences” matter if my record counts match?</strong></summary>

Counts can match while behavior is wrong. What matters is whether relationships work: variants purchase correctly, categories browse logically, and orders remain linked to the right customers.

</details>
