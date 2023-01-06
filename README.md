# Horizon deployment Template
The deployment horizon template is a simple example of a Horizon template.

The template contains a single kubernetes resource [deployment](https://kubernetes.io/docs/concepts/workloads/controllers/deployment/) resource


Simple options are exposed to users based on [jsonschema](https://json-schema.org/) and [react-jsonschema-form](https://github.com/rjsf-team/react-jsonschema-form)

* **Spec**: Template provides optional specifications (tiny(0.5C 1G), x-small(1C2G), sample(2C4G), middle(4C8G)), 
* **Replicas**: Optional number of replicas, default maximum 30
* **Envs**: Environment Variables array

ps:  open  larger and flexible Spec by add admin tag to the cluster (key: supportMoreSpecs, value:large,flexible)

ps:  extent maxReplica by add admin tag to cluster (key: maxReplicas, value:50)


## Structure
```
.
├── Chart.yaml
├── LICENSE
├── README.md
├── schema
│   ├── application.schema.json
│   └── application.ui.schema.json
├── templates
│   ├── _helpers.tpl
│   └── deployment.yaml
└── values.yaml
```

* Chart.yaml: helm chart file
* Value.yaml: helm value file
* Template: the template resource files
* schema: jsonschema and react-jsonschema-form file


## Horizon template

Horizon Template is based on helm, jsonschema and react-jsonschema-form.  It is flexible and customizable just like helm template, The Platform Team can make the basic practice (including security, affinity, priority, resource, etc.) by default, and provide user a simple and uniform interface which is defined by jsonschema files. jsonschema is used for provide a user friend HTML form on the Horizon Based on react-jsonschema-form. 

It's highly Scalable and flexible to make your own best practice based on the simple template system.


