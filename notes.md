# 20250514

LogicalPlan defined in: `datafusion/expr/src/logical_plan/plan.rs`

Dataframe call to describe in: `datafusion/core/src/dataframe/mod.rs`

Dataframe call gets schema name from schema which is called on the logical plan.

Seems like schema call on logicalplan would return some kind of query ast / substrait type thingy.

Gut feeling is that the bug occurs in aggregation of the describe call using a get column by name
command in the final report build but the plan might conform identifiers to lower casing and ignore
non alnum characters to ease schema merging.


