---
description: Variables allow you to store and reuse values in n8n workflows. 
---

# Variables

!!! info "Feature availability"
	* Available on Self-hosted Enterprise and Power Cloud plans.
	* You need access to the n8n instance owner account to create and edit variables. All users can use existing variables.

	Available in verion [TODO] and above.

Variables allow you to store and reuse values in n8n workflows. 

!!! warning "Variables are shared"
	When you create a variable, it's available to everyone on your n8n instance.

## Create variables

To create a new variable:

1. On the **Variables** page, select **Add Variable**.
3. Enter a **Key** and **Value**.
4. Select **Save**. The variable is now available for use in all workflows in the n8n instance.

## Edit and delete variables

To edit or delete a variable:

1. On the **Variables** page, hover over the variable you want to change.
2. Select **Edit** or **Delete**.

## Use variables in workflows

You can use variables in the Code node and in expressions:

```javascript
// Access a variable
$vars.<variable-name>
```

All variables are strings.

During workflow execution, n8n replaces the variables with the variable value. If the variable has no value, n8n treats its value as `undefined`. Workflows don't automatically fail in this case.