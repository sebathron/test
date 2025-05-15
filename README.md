# How make a new build
install npm and yarn (sudo npm install -g yarn)
npx run projen
npm install --save-dev
change version on package.json ("version": "x.x.x")
npm run docgen && npm run eslint && npm run compile && npm run package
export TWINE_USERNAME=aws
export TWINE_PASSWORD=`aws codeartifact get-authorization-token --domain thron --domain-owner 499570923361 --region eu-west-1 --query authorizationToken --output text`
export TWINE_REPOSITORY_URL=`aws codeartifact get-repository-endpoint --domain thron --domain-owner 499570923361 --repository pypi-store --region eu-west-1 --format pypi --query repositoryEndpoint --output text`
npx -p publib@latest publib-pypi

# Project Title

One Paragraph of project description goes here

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes. See deployment for notes on how to deploy the project on a live system.

### Prerequisites

What things you need to install the software and how to install them

```
Give examples
```

### Installing

A step by step series of examples that tell you how to get a development env running

Say what the step will be

```
Give the example
```

And repeat

```
until finished
```

End with an example of getting some data out of the system or using it for a little demo

## Running the tests

Explain how to run the automated tests for this system

### Break down into end to end tests

Explain what these tests test and why

```
Give an example
```

### And coding style tests

Explain what these tests test and why

```
Give an example
```

## Deployment

Add additional notes about how to deploy this on a live system

## Built With

* [Dropwizard](http://www.dropwizard.io/1.0.2/docs/) - The web framework used
* [Maven](https://maven.apache.org/) - Dependency Management
* [ROME](https://rometools.github.io/rome/) - Used to generate RSS Feeds

## Acknowledgments

* Hat tip to anyone whose code was used
* Inspiration
* etc


<!-- TWINE PASSWORD  -->
<!-- aws codeartifact get-authorization-token --domain thron --domain-owner 499570923361 --query authorizationToken --output text -->
# API Reference <a name="API Reference" id="api-reference"></a>

## Constructs <a name="Constructs" id="Constructs"></a>

### DefaultValue <a name="DefaultValue" id="cdk-constructs.DefaultValue"></a>

#### Initializers <a name="Initializers" id="cdk-constructs.DefaultValue.Initializer"></a>

```typescript
import { DefaultValue } from 'cdk-constructs'

new DefaultValue(scope: Construct, id: string)
```

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.DefaultValue.Initializer.parameter.scope">scope</a></code> | <code>constructs.Construct</code> | *No description.* |
| <code><a href="#cdk-constructs.DefaultValue.Initializer.parameter.id">id</a></code> | <code>string</code> | *No description.* |

---

##### `scope`<sup>Required</sup> <a name="scope" id="cdk-constructs.DefaultValue.Initializer.parameter.scope"></a>

- *Type:* constructs.Construct

---

##### `id`<sup>Required</sup> <a name="id" id="cdk-constructs.DefaultValue.Initializer.parameter.id"></a>

- *Type:* string

---

#### Methods <a name="Methods" id="Methods"></a>

| **Name** | **Description** |
| --- | --- |
| <code><a href="#cdk-constructs.DefaultValue.toString">toString</a></code> | Returns a string representation of this construct. |
| <code><a href="#cdk-constructs.DefaultValue.cdnDomainLong">cdnDomainLong</a></code> | *No description.* |
| <code><a href="#cdk-constructs.DefaultValue.privateRouteR53Zone">privateRouteR53Zone</a></code> | *No description.* |
| <code><a href="#cdk-constructs.DefaultValue.privateSubnetSelection">privateSubnetSelection</a></code> | *No description.* |
| <code><a href="#cdk-constructs.DefaultValue.sitename">sitename</a></code> | *No description.* |
| <code><a href="#cdk-constructs.DefaultValue.vpc">vpc</a></code> | *No description.* |
| <code><a href="#cdk-constructs.DefaultValue.vpcId">vpcId</a></code> | *No description.* |
| <code><a href="#cdk-constructs.DefaultValue.vpcIPV4Cidr">vpcIPV4Cidr</a></code> | *No description.* |
| <code><a href="#cdk-constructs.DefaultValue.vpcIPV6Cidr">vpcIPV6Cidr</a></code> | *No description.* |

---

##### `toString` <a name="toString" id="cdk-constructs.DefaultValue.toString"></a>

```typescript
public toString(): string
```

Returns a string representation of this construct.

##### `cdnDomainLong` <a name="cdnDomainLong" id="cdk-constructs.DefaultValue.cdnDomainLong"></a>

```typescript
public cdnDomainLong(): string
```

##### `privateRouteR53Zone` <a name="privateRouteR53Zone" id="cdk-constructs.DefaultValue.privateRouteR53Zone"></a>

```typescript
public privateRouteR53Zone(): IHostedZone
```

##### `privateSubnetSelection` <a name="privateSubnetSelection" id="cdk-constructs.DefaultValue.privateSubnetSelection"></a>

```typescript
public privateSubnetSelection(): SubnetSelection
```

##### `sitename` <a name="sitename" id="cdk-constructs.DefaultValue.sitename"></a>

```typescript
public sitename(): string
```

##### `vpc` <a name="vpc" id="cdk-constructs.DefaultValue.vpc"></a>

```typescript
public vpc(): IVpc
```

##### `vpcId` <a name="vpcId" id="cdk-constructs.DefaultValue.vpcId"></a>

```typescript
public vpcId(): string
```

##### `vpcIPV4Cidr` <a name="vpcIPV4Cidr" id="cdk-constructs.DefaultValue.vpcIPV4Cidr"></a>

```typescript
public vpcIPV4Cidr(): string
```

##### `vpcIPV6Cidr` <a name="vpcIPV6Cidr" id="cdk-constructs.DefaultValue.vpcIPV6Cidr"></a>

```typescript
public vpcIPV6Cidr(): string
```

#### Static Functions <a name="Static Functions" id="Static Functions"></a>

| **Name** | **Description** |
| --- | --- |
| <code><a href="#cdk-constructs.DefaultValue.isConstruct">isConstruct</a></code> | Checks if `x` is a construct. |

---

##### `isConstruct` <a name="isConstruct" id="cdk-constructs.DefaultValue.isConstruct"></a>

```typescript
import { DefaultValue } from 'cdk-constructs'

DefaultValue.isConstruct(x: any)
```

Checks if `x` is a construct.

Use this method instead of `instanceof` to properly detect `Construct`
instances, even when the construct library is symlinked.

Explanation: in JavaScript, multiple copies of the `constructs` library on
disk are seen as independent, completely different libraries. As a
consequence, the class `Construct` in each copy of the `constructs` library
is seen as a different class, and an instance of one class will not test as
`instanceof` the other class. `npm install` will not create installations
like this, but users may manually symlink construct libraries together or
use a monorepo tool: in those cases, multiple copies of the `constructs`
library can be accidentally installed, and `instanceof` will behave
unpredictably. It is safest to avoid using `instanceof`, and using
this type-testing method instead.

###### `x`<sup>Required</sup> <a name="x" id="cdk-constructs.DefaultValue.isConstruct.parameter.x"></a>

- *Type:* any

Any object.

---

#### Properties <a name="Properties" id="Properties"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.DefaultValue.property.node">node</a></code> | <code>constructs.Node</code> | The tree node. |

---

##### `node`<sup>Required</sup> <a name="node" id="cdk-constructs.DefaultValue.property.node"></a>

```typescript
public readonly node: Node;
```

- *Type:* constructs.Node

The tree node.

---


### DockerBuildAndPush <a name="DockerBuildAndPush" id="cdk-constructs.DockerBuildAndPush"></a>

#### Initializers <a name="Initializers" id="cdk-constructs.DockerBuildAndPush.Initializer"></a>

```typescript
import { DockerBuildAndPush } from 'cdk-constructs'

new DockerBuildAndPush(scope: Stack, id: string, directory: string, dockerfile?: string)
```

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.DockerBuildAndPush.Initializer.parameter.scope">scope</a></code> | <code>aws-cdk-lib.Stack</code> | *No description.* |
| <code><a href="#cdk-constructs.DockerBuildAndPush.Initializer.parameter.id">id</a></code> | <code>string</code> | *No description.* |
| <code><a href="#cdk-constructs.DockerBuildAndPush.Initializer.parameter.directory">directory</a></code> | <code>string</code> | *No description.* |
| <code><a href="#cdk-constructs.DockerBuildAndPush.Initializer.parameter.dockerfile">dockerfile</a></code> | <code>string</code> | *No description.* |

---

##### `scope`<sup>Required</sup> <a name="scope" id="cdk-constructs.DockerBuildAndPush.Initializer.parameter.scope"></a>

- *Type:* aws-cdk-lib.Stack

---

##### `id`<sup>Required</sup> <a name="id" id="cdk-constructs.DockerBuildAndPush.Initializer.parameter.id"></a>

- *Type:* string

---

##### `directory`<sup>Required</sup> <a name="directory" id="cdk-constructs.DockerBuildAndPush.Initializer.parameter.directory"></a>

- *Type:* string

---

##### `dockerfile`<sup>Optional</sup> <a name="dockerfile" id="cdk-constructs.DockerBuildAndPush.Initializer.parameter.dockerfile"></a>

- *Type:* string

---

#### Methods <a name="Methods" id="Methods"></a>

| **Name** | **Description** |
| --- | --- |
| <code><a href="#cdk-constructs.DockerBuildAndPush.toString">toString</a></code> | Returns a string representation of this construct. |
| <code><a href="#cdk-constructs.DockerBuildAndPush.addDependency">addDependency</a></code> | Add a dependency between this stack and another stack. |
| <code><a href="#cdk-constructs.DockerBuildAndPush.addMetadata">addMetadata</a></code> | Adds an arbitrary key-value pair, with information you want to record about the stack. |
| <code><a href="#cdk-constructs.DockerBuildAndPush.addTransform">addTransform</a></code> | Add a Transform to this stack. A Transform is a macro that AWS CloudFormation uses to process your template. |
| <code><a href="#cdk-constructs.DockerBuildAndPush.exportStringListValue">exportStringListValue</a></code> | Create a CloudFormation Export for a string list value. |
| <code><a href="#cdk-constructs.DockerBuildAndPush.exportValue">exportValue</a></code> | Create a CloudFormation Export for a string value. |
| <code><a href="#cdk-constructs.DockerBuildAndPush.formatArn">formatArn</a></code> | Creates an ARN from components. |
| <code><a href="#cdk-constructs.DockerBuildAndPush.getLogicalId">getLogicalId</a></code> | Allocates a stack-unique CloudFormation-compatible logical identity for a specific resource. |
| <code><a href="#cdk-constructs.DockerBuildAndPush.regionalFact">regionalFact</a></code> | Look up a fact value for the given fact for the region of this stack. |
| <code><a href="#cdk-constructs.DockerBuildAndPush.renameLogicalId">renameLogicalId</a></code> | Rename a generated logical identities. |
| <code><a href="#cdk-constructs.DockerBuildAndPush.reportMissingContextKey">reportMissingContextKey</a></code> | Indicate that a context key was expected. |
| <code><a href="#cdk-constructs.DockerBuildAndPush.resolve">resolve</a></code> | Resolve a tokenized value in the context of the current stack. |
| <code><a href="#cdk-constructs.DockerBuildAndPush.splitArn">splitArn</a></code> | Splits the provided ARN into its components. |
| <code><a href="#cdk-constructs.DockerBuildAndPush.toJsonString">toJsonString</a></code> | Convert an object, potentially containing tokens, to a JSON string. |
| <code><a href="#cdk-constructs.DockerBuildAndPush.toYamlString">toYamlString</a></code> | Convert an object, potentially containing tokens, to a YAML string. |

---

##### `toString` <a name="toString" id="cdk-constructs.DockerBuildAndPush.toString"></a>

```typescript
public toString(): string
```

Returns a string representation of this construct.

##### `addDependency` <a name="addDependency" id="cdk-constructs.DockerBuildAndPush.addDependency"></a>

```typescript
public addDependency(target: Stack, reason?: string): void
```

Add a dependency between this stack and another stack.

This can be used to define dependencies between any two stacks within an
app, and also supports nested stacks.

###### `target`<sup>Required</sup> <a name="target" id="cdk-constructs.DockerBuildAndPush.addDependency.parameter.target"></a>

- *Type:* aws-cdk-lib.Stack

---

###### `reason`<sup>Optional</sup> <a name="reason" id="cdk-constructs.DockerBuildAndPush.addDependency.parameter.reason"></a>

- *Type:* string

---

##### `addMetadata` <a name="addMetadata" id="cdk-constructs.DockerBuildAndPush.addMetadata"></a>

```typescript
public addMetadata(key: string, value: any): void
```

Adds an arbitrary key-value pair, with information you want to record about the stack.

These get translated to the Metadata section of the generated template.

> [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/metadata-section-structure.html](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/metadata-section-structure.html)

###### `key`<sup>Required</sup> <a name="key" id="cdk-constructs.DockerBuildAndPush.addMetadata.parameter.key"></a>

- *Type:* string

---

###### `value`<sup>Required</sup> <a name="value" id="cdk-constructs.DockerBuildAndPush.addMetadata.parameter.value"></a>

- *Type:* any

---

##### `addTransform` <a name="addTransform" id="cdk-constructs.DockerBuildAndPush.addTransform"></a>

```typescript
public addTransform(transform: string): void
```

Add a Transform to this stack. A Transform is a macro that AWS CloudFormation uses to process your template.

Duplicate values are removed when stack is synthesized.

> [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/transform-section-structure.html](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/transform-section-structure.html)

*Example*

```typescript
declare const stack: Stack;

stack.addTransform('AWS::Serverless-2016-10-31')
```


###### `transform`<sup>Required</sup> <a name="transform" id="cdk-constructs.DockerBuildAndPush.addTransform.parameter.transform"></a>

- *Type:* string

The transform to add.

---

##### `exportStringListValue` <a name="exportStringListValue" id="cdk-constructs.DockerBuildAndPush.exportStringListValue"></a>

```typescript
public exportStringListValue(exportedValue: any, options?: ExportValueOptions): string[]
```

Create a CloudFormation Export for a string list value.

Returns a string list representing the corresponding `Fn.importValue()`
expression for this Export. The export expression is automatically wrapped with an
`Fn::Join` and the import value with an `Fn::Split`, since CloudFormation can only
export strings. You can control the name for the export by passing the `name` option.

If you don't supply a value for `name`, the value you're exporting must be
a Resource attribute (for example: `bucket.bucketName`) and it will be
given the same name as the automatic cross-stack reference that would be created
if you used the attribute in another Stack.

One of the uses for this method is to *remove* the relationship between
two Stacks established by automatic cross-stack references. It will
temporarily ensure that the CloudFormation Export still exists while you
remove the reference from the consuming stack. After that, you can remove
the resource and the manual export.

See `exportValue` for an example of this process.

###### `exportedValue`<sup>Required</sup> <a name="exportedValue" id="cdk-constructs.DockerBuildAndPush.exportStringListValue.parameter.exportedValue"></a>

- *Type:* any

---

###### `options`<sup>Optional</sup> <a name="options" id="cdk-constructs.DockerBuildAndPush.exportStringListValue.parameter.options"></a>

- *Type:* aws-cdk-lib.ExportValueOptions

---

##### `exportValue` <a name="exportValue" id="cdk-constructs.DockerBuildAndPush.exportValue"></a>

```typescript
public exportValue(exportedValue: any, options?: ExportValueOptions): string
```

Create a CloudFormation Export for a string value.

Returns a string representing the corresponding `Fn.importValue()`
expression for this Export. You can control the name for the export by
passing the `name` option.

If you don't supply a value for `name`, the value you're exporting must be
a Resource attribute (for example: `bucket.bucketName`) and it will be
given the same name as the automatic cross-stack reference that would be created
if you used the attribute in another Stack.

One of the uses for this method is to *remove* the relationship between
two Stacks established by automatic cross-stack references. It will
temporarily ensure that the CloudFormation Export still exists while you
remove the reference from the consuming stack. After that, you can remove
the resource and the manual export.

Here is how the process works. Let's say there are two stacks,
`producerStack` and `consumerStack`, and `producerStack` has a bucket
called `bucket`, which is referenced by `consumerStack` (perhaps because
an AWS Lambda Function writes into it, or something like that).

It is not safe to remove `producerStack.bucket` because as the bucket is being
deleted, `consumerStack` might still be using it.

Instead, the process takes two deployments:

**Deployment 1: break the relationship**:

- Make sure `consumerStack` no longer references `bucket.bucketName` (maybe the consumer
  stack now uses its own bucket, or it writes to an AWS DynamoDB table, or maybe you just
  remove the Lambda Function altogether).
- In the `ProducerStack` class, call `this.exportValue(this.bucket.bucketName)`. This
  will make sure the CloudFormation Export continues to exist while the relationship
  between the two stacks is being broken.
- Deploy (this will effectively only change the `consumerStack`, but it's safe to deploy both).

**Deployment 2: remove the bucket resource**:

- You are now free to remove the `bucket` resource from `producerStack`.
- Don't forget to remove the `exportValue()` call as well.
- Deploy again (this time only the `producerStack` will be changed -- the bucket will be deleted).

###### `exportedValue`<sup>Required</sup> <a name="exportedValue" id="cdk-constructs.DockerBuildAndPush.exportValue.parameter.exportedValue"></a>

- *Type:* any

---

###### `options`<sup>Optional</sup> <a name="options" id="cdk-constructs.DockerBuildAndPush.exportValue.parameter.options"></a>

- *Type:* aws-cdk-lib.ExportValueOptions

---

##### `formatArn` <a name="formatArn" id="cdk-constructs.DockerBuildAndPush.formatArn"></a>

```typescript
public formatArn(components: ArnComponents): string
```

Creates an ARN from components.

If `partition`, `region` or `account` are not specified, the stack's
partition, region and account will be used.

If any component is the empty string, an empty string will be inserted
into the generated ARN at the location that component corresponds to.

The ARN will be formatted as follows:

  arn:{partition}:{service}:{region}:{account}:{resource}{sep}{resource-name}

The required ARN pieces that are omitted will be taken from the stack that
the 'scope' is attached to. If all ARN pieces are supplied, the supplied scope
can be 'undefined'.

###### `components`<sup>Required</sup> <a name="components" id="cdk-constructs.DockerBuildAndPush.formatArn.parameter.components"></a>

- *Type:* aws-cdk-lib.ArnComponents

---

##### `getLogicalId` <a name="getLogicalId" id="cdk-constructs.DockerBuildAndPush.getLogicalId"></a>

```typescript
public getLogicalId(element: CfnElement): string
```

Allocates a stack-unique CloudFormation-compatible logical identity for a specific resource.

This method is called when a `CfnElement` is created and used to render the
initial logical identity of resources. Logical ID renames are applied at
this stage.

This method uses the protected method `allocateLogicalId` to render the
logical ID for an element. To modify the naming scheme, extend the `Stack`
class and override this method.

###### `element`<sup>Required</sup> <a name="element" id="cdk-constructs.DockerBuildAndPush.getLogicalId.parameter.element"></a>

- *Type:* aws-cdk-lib.CfnElement

The CloudFormation element for which a logical identity is needed.

---

##### `regionalFact` <a name="regionalFact" id="cdk-constructs.DockerBuildAndPush.regionalFact"></a>

```typescript
public regionalFact(factName: string, defaultValue?: string): string
```

Look up a fact value for the given fact for the region of this stack.

Will return a definite value only if the region of the current stack is resolved.
If not, a lookup map will be added to the stack and the lookup will be done at
CDK deployment time.

What regions will be included in the lookup map is controlled by the
`@aws-cdk/core:target-partitions` context value: it must be set to a list
of partitions, and only regions from the given partitions will be included.
If no such context key is set, all regions will be included.

This function is intended to be used by construct library authors. Application
builders can rely on the abstractions offered by construct libraries and do
not have to worry about regional facts.

If `defaultValue` is not given, it is an error if the fact is unknown for
the given region.

###### `factName`<sup>Required</sup> <a name="factName" id="cdk-constructs.DockerBuildAndPush.regionalFact.parameter.factName"></a>

- *Type:* string

---

###### `defaultValue`<sup>Optional</sup> <a name="defaultValue" id="cdk-constructs.DockerBuildAndPush.regionalFact.parameter.defaultValue"></a>

- *Type:* string

---

##### `renameLogicalId` <a name="renameLogicalId" id="cdk-constructs.DockerBuildAndPush.renameLogicalId"></a>

```typescript
public renameLogicalId(oldId: string, newId: string): void
```

Rename a generated logical identities.

To modify the naming scheme strategy, extend the `Stack` class and
override the `allocateLogicalId` method.

###### `oldId`<sup>Required</sup> <a name="oldId" id="cdk-constructs.DockerBuildAndPush.renameLogicalId.parameter.oldId"></a>

- *Type:* string

---

###### `newId`<sup>Required</sup> <a name="newId" id="cdk-constructs.DockerBuildAndPush.renameLogicalId.parameter.newId"></a>

- *Type:* string

---

##### `reportMissingContextKey` <a name="reportMissingContextKey" id="cdk-constructs.DockerBuildAndPush.reportMissingContextKey"></a>

```typescript
public reportMissingContextKey(report: MissingContext): void
```

Indicate that a context key was expected.

Contains instructions which will be emitted into the cloud assembly on how
the key should be supplied.

###### `report`<sup>Required</sup> <a name="report" id="cdk-constructs.DockerBuildAndPush.reportMissingContextKey.parameter.report"></a>

- *Type:* aws-cdk-lib.cloud_assembly_schema.MissingContext

The set of parameters needed to obtain the context.

---

##### `resolve` <a name="resolve" id="cdk-constructs.DockerBuildAndPush.resolve"></a>

```typescript
public resolve(obj: any): any
```

Resolve a tokenized value in the context of the current stack.

###### `obj`<sup>Required</sup> <a name="obj" id="cdk-constructs.DockerBuildAndPush.resolve.parameter.obj"></a>

- *Type:* any

---

##### `splitArn` <a name="splitArn" id="cdk-constructs.DockerBuildAndPush.splitArn"></a>

```typescript
public splitArn(arn: string, arnFormat: ArnFormat): ArnComponents
```

Splits the provided ARN into its components.

Works both if 'arn' is a string like 'arn:aws:s3:::bucket',
and a Token representing a dynamic CloudFormation expression
(in which case the returned components will also be dynamic CloudFormation expressions,
encoded as Tokens).

###### `arn`<sup>Required</sup> <a name="arn" id="cdk-constructs.DockerBuildAndPush.splitArn.parameter.arn"></a>

- *Type:* string

the ARN to split into its components.

---

###### `arnFormat`<sup>Required</sup> <a name="arnFormat" id="cdk-constructs.DockerBuildAndPush.splitArn.parameter.arnFormat"></a>

- *Type:* aws-cdk-lib.ArnFormat

the expected format of 'arn' - depends on what format the service 'arn' represents uses.

---

##### `toJsonString` <a name="toJsonString" id="cdk-constructs.DockerBuildAndPush.toJsonString"></a>

```typescript
public toJsonString(obj: any, space?: number): string
```

Convert an object, potentially containing tokens, to a JSON string.

###### `obj`<sup>Required</sup> <a name="obj" id="cdk-constructs.DockerBuildAndPush.toJsonString.parameter.obj"></a>

- *Type:* any

---

###### `space`<sup>Optional</sup> <a name="space" id="cdk-constructs.DockerBuildAndPush.toJsonString.parameter.space"></a>

- *Type:* number

---

##### `toYamlString` <a name="toYamlString" id="cdk-constructs.DockerBuildAndPush.toYamlString"></a>

```typescript
public toYamlString(obj: any): string
```

Convert an object, potentially containing tokens, to a YAML string.

###### `obj`<sup>Required</sup> <a name="obj" id="cdk-constructs.DockerBuildAndPush.toYamlString.parameter.obj"></a>

- *Type:* any

---

#### Static Functions <a name="Static Functions" id="Static Functions"></a>

| **Name** | **Description** |
| --- | --- |
| <code><a href="#cdk-constructs.DockerBuildAndPush.isConstruct">isConstruct</a></code> | Checks if `x` is a construct. |
| <code><a href="#cdk-constructs.DockerBuildAndPush.isStack">isStack</a></code> | Return whether the given object is a Stack. |
| <code><a href="#cdk-constructs.DockerBuildAndPush.of">of</a></code> | Looks up the first stack scope in which `construct` is defined. |

---

##### `isConstruct` <a name="isConstruct" id="cdk-constructs.DockerBuildAndPush.isConstruct"></a>

```typescript
import { DockerBuildAndPush } from 'cdk-constructs'

DockerBuildAndPush.isConstruct(x: any)
```

Checks if `x` is a construct.

Use this method instead of `instanceof` to properly detect `Construct`
instances, even when the construct library is symlinked.

Explanation: in JavaScript, multiple copies of the `constructs` library on
disk are seen as independent, completely different libraries. As a
consequence, the class `Construct` in each copy of the `constructs` library
is seen as a different class, and an instance of one class will not test as
`instanceof` the other class. `npm install` will not create installations
like this, but users may manually symlink construct libraries together or
use a monorepo tool: in those cases, multiple copies of the `constructs`
library can be accidentally installed, and `instanceof` will behave
unpredictably. It is safest to avoid using `instanceof`, and using
this type-testing method instead.

###### `x`<sup>Required</sup> <a name="x" id="cdk-constructs.DockerBuildAndPush.isConstruct.parameter.x"></a>

- *Type:* any

Any object.

---

##### `isStack` <a name="isStack" id="cdk-constructs.DockerBuildAndPush.isStack"></a>

```typescript
import { DockerBuildAndPush } from 'cdk-constructs'

DockerBuildAndPush.isStack(x: any)
```

Return whether the given object is a Stack.

We do attribute detection since we can't reliably use 'instanceof'.

###### `x`<sup>Required</sup> <a name="x" id="cdk-constructs.DockerBuildAndPush.isStack.parameter.x"></a>

- *Type:* any

---

##### `of` <a name="of" id="cdk-constructs.DockerBuildAndPush.of"></a>

```typescript
import { DockerBuildAndPush } from 'cdk-constructs'

DockerBuildAndPush.of(construct: IConstruct)
```

Looks up the first stack scope in which `construct` is defined.

Fails if there is no stack up the tree.

###### `construct`<sup>Required</sup> <a name="construct" id="cdk-constructs.DockerBuildAndPush.of.parameter.construct"></a>

- *Type:* constructs.IConstruct

The construct to start the search from.

---

#### Properties <a name="Properties" id="Properties"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.DockerBuildAndPush.property.node">node</a></code> | <code>constructs.Node</code> | The tree node. |
| <code><a href="#cdk-constructs.DockerBuildAndPush.property.account">account</a></code> | <code>string</code> | The AWS account into which this stack will be deployed. |
| <code><a href="#cdk-constructs.DockerBuildAndPush.property.artifactId">artifactId</a></code> | <code>string</code> | The ID of the cloud assembly artifact for this stack. |
| <code><a href="#cdk-constructs.DockerBuildAndPush.property.availabilityZones">availabilityZones</a></code> | <code>string[]</code> | Returns the list of AZs that are available in the AWS environment (account/region) associated with this stack. |
| <code><a href="#cdk-constructs.DockerBuildAndPush.property.bundlingRequired">bundlingRequired</a></code> | <code>boolean</code> | Indicates whether the stack requires bundling or not. |
| <code><a href="#cdk-constructs.DockerBuildAndPush.property.dependencies">dependencies</a></code> | <code>aws-cdk-lib.Stack[]</code> | Return the stacks this stack depends on. |
| <code><a href="#cdk-constructs.DockerBuildAndPush.property.environment">environment</a></code> | <code>string</code> | The environment coordinates in which this stack is deployed. |
| <code><a href="#cdk-constructs.DockerBuildAndPush.property.nested">nested</a></code> | <code>boolean</code> | Indicates if this is a nested stack, in which case `parentStack` will include a reference to it's parent. |
| <code><a href="#cdk-constructs.DockerBuildAndPush.property.notificationArns">notificationArns</a></code> | <code>string[]</code> | Returns the list of notification Amazon Resource Names (ARNs) for the current stack. |
| <code><a href="#cdk-constructs.DockerBuildAndPush.property.partition">partition</a></code> | <code>string</code> | The partition in which this stack is defined. |
| <code><a href="#cdk-constructs.DockerBuildAndPush.property.region">region</a></code> | <code>string</code> | The AWS region into which this stack will be deployed (e.g. `us-west-2`). |
| <code><a href="#cdk-constructs.DockerBuildAndPush.property.stackId">stackId</a></code> | <code>string</code> | The ID of the stack. |
| <code><a href="#cdk-constructs.DockerBuildAndPush.property.stackName">stackName</a></code> | <code>string</code> | The concrete CloudFormation physical stack name. |
| <code><a href="#cdk-constructs.DockerBuildAndPush.property.synthesizer">synthesizer</a></code> | <code>aws-cdk-lib.IStackSynthesizer</code> | Synthesis method for this stack. |
| <code><a href="#cdk-constructs.DockerBuildAndPush.property.tags">tags</a></code> | <code>aws-cdk-lib.TagManager</code> | Tags to be applied to the stack. |
| <code><a href="#cdk-constructs.DockerBuildAndPush.property.templateFile">templateFile</a></code> | <code>string</code> | The name of the CloudFormation template file emitted to the output directory during synthesis. |
| <code><a href="#cdk-constructs.DockerBuildAndPush.property.templateOptions">templateOptions</a></code> | <code>aws-cdk-lib.ITemplateOptions</code> | Options for CloudFormation template (like version, transform, description). |
| <code><a href="#cdk-constructs.DockerBuildAndPush.property.urlSuffix">urlSuffix</a></code> | <code>string</code> | The Amazon domain suffix for the region in which this stack is defined. |
| <code><a href="#cdk-constructs.DockerBuildAndPush.property.nestedStackParent">nestedStackParent</a></code> | <code>aws-cdk-lib.Stack</code> | If this is a nested stack, returns it's parent stack. |
| <code><a href="#cdk-constructs.DockerBuildAndPush.property.nestedStackResource">nestedStackResource</a></code> | <code>aws-cdk-lib.CfnResource</code> | If this is a nested stack, this represents its `AWS::CloudFormation::Stack` resource. |
| <code><a href="#cdk-constructs.DockerBuildAndPush.property.terminationProtection">terminationProtection</a></code> | <code>boolean</code> | Whether termination protection is enabled for this stack. |
| <code><a href="#cdk-constructs.DockerBuildAndPush.property.ecrImage">ecrImage</a></code> | <code>aws-cdk-lib.aws_ecs.EcrImage</code> | *No description.* |
| <code><a href="#cdk-constructs.DockerBuildAndPush.property.lambdaDockerImageCode">lambdaDockerImageCode</a></code> | <code>aws-cdk-lib.aws_lambda.DockerImageCode</code> | *No description.* |

---

##### `node`<sup>Required</sup> <a name="node" id="cdk-constructs.DockerBuildAndPush.property.node"></a>

```typescript
public readonly node: Node;
```

- *Type:* constructs.Node

The tree node.

---

##### `account`<sup>Required</sup> <a name="account" id="cdk-constructs.DockerBuildAndPush.property.account"></a>

```typescript
public readonly account: string;
```

- *Type:* string

The AWS account into which this stack will be deployed.

This value is resolved according to the following rules:

1. The value provided to `env.account` when the stack is defined. This can
   either be a concrete account (e.g. `585695031111`) or the
   `Aws.ACCOUNT_ID` token.
3. `Aws.ACCOUNT_ID`, which represents the CloudFormation intrinsic reference
   `{ "Ref": "AWS::AccountId" }` encoded as a string token.

Preferably, you should use the return value as an opaque string and not
attempt to parse it to implement your logic. If you do, you must first
check that it is a concrete value an not an unresolved token. If this
value is an unresolved token (`Token.isUnresolved(stack.account)` returns
`true`), this implies that the user wishes that this stack will synthesize
into an **account-agnostic template**. In this case, your code should either
fail (throw an error, emit a synth error using `Annotations.of(construct).addError()`) or
implement some other account-agnostic behavior.

---

##### `artifactId`<sup>Required</sup> <a name="artifactId" id="cdk-constructs.DockerBuildAndPush.property.artifactId"></a>

```typescript
public readonly artifactId: string;
```

- *Type:* string

The ID of the cloud assembly artifact for this stack.

---

##### `availabilityZones`<sup>Required</sup> <a name="availabilityZones" id="cdk-constructs.DockerBuildAndPush.property.availabilityZones"></a>

```typescript
public readonly availabilityZones: string[];
```

- *Type:* string[]

Returns the list of AZs that are available in the AWS environment (account/region) associated with this stack.

If the stack is environment-agnostic (either account and/or region are
tokens), this property will return an array with 2 tokens that will resolve
at deploy-time to the first two availability zones returned from CloudFormation's
`Fn::GetAZs` intrinsic function.

If they are not available in the context, returns a set of dummy values and
reports them as missing, and let the CLI resolve them by calling EC2
`DescribeAvailabilityZones` on the target environment.

To specify a different strategy for selecting availability zones override this method.

---

##### `bundlingRequired`<sup>Required</sup> <a name="bundlingRequired" id="cdk-constructs.DockerBuildAndPush.property.bundlingRequired"></a>

```typescript
public readonly bundlingRequired: boolean;
```

- *Type:* boolean

Indicates whether the stack requires bundling or not.

---

##### `dependencies`<sup>Required</sup> <a name="dependencies" id="cdk-constructs.DockerBuildAndPush.property.dependencies"></a>

```typescript
public readonly dependencies: Stack[];
```

- *Type:* aws-cdk-lib.Stack[]

Return the stacks this stack depends on.

---

##### `environment`<sup>Required</sup> <a name="environment" id="cdk-constructs.DockerBuildAndPush.property.environment"></a>

```typescript
public readonly environment: string;
```

- *Type:* string

The environment coordinates in which this stack is deployed.

In the form
`aws://account/region`. Use `stack.account` and `stack.region` to obtain
the specific values, no need to parse.

You can use this value to determine if two stacks are targeting the same
environment.

If either `stack.account` or `stack.region` are not concrete values (e.g.
`Aws.ACCOUNT_ID` or `Aws.REGION`) the special strings `unknown-account` and/or
`unknown-region` will be used respectively to indicate this stack is
region/account-agnostic.

---

##### `nested`<sup>Required</sup> <a name="nested" id="cdk-constructs.DockerBuildAndPush.property.nested"></a>

```typescript
public readonly nested: boolean;
```

- *Type:* boolean

Indicates if this is a nested stack, in which case `parentStack` will include a reference to it's parent.

---

##### `notificationArns`<sup>Required</sup> <a name="notificationArns" id="cdk-constructs.DockerBuildAndPush.property.notificationArns"></a>

```typescript
public readonly notificationArns: string[];
```

- *Type:* string[]

Returns the list of notification Amazon Resource Names (ARNs) for the current stack.

---

##### `partition`<sup>Required</sup> <a name="partition" id="cdk-constructs.DockerBuildAndPush.property.partition"></a>

```typescript
public readonly partition: string;
```

- *Type:* string

The partition in which this stack is defined.

---

##### `region`<sup>Required</sup> <a name="region" id="cdk-constructs.DockerBuildAndPush.property.region"></a>

```typescript
public readonly region: string;
```

- *Type:* string

The AWS region into which this stack will be deployed (e.g. `us-west-2`).

This value is resolved according to the following rules:

1. The value provided to `env.region` when the stack is defined. This can
   either be a concrete region (e.g. `us-west-2`) or the `Aws.REGION`
   token.
3. `Aws.REGION`, which is represents the CloudFormation intrinsic reference
   `{ "Ref": "AWS::Region" }` encoded as a string token.

Preferably, you should use the return value as an opaque string and not
attempt to parse it to implement your logic. If you do, you must first
check that it is a concrete value an not an unresolved token. If this
value is an unresolved token (`Token.isUnresolved(stack.region)` returns
`true`), this implies that the user wishes that this stack will synthesize
into a **region-agnostic template**. In this case, your code should either
fail (throw an error, emit a synth error using `Annotations.of(construct).addError()`) or
implement some other region-agnostic behavior.

---

##### `stackId`<sup>Required</sup> <a name="stackId" id="cdk-constructs.DockerBuildAndPush.property.stackId"></a>

```typescript
public readonly stackId: string;
```

- *Type:* string

The ID of the stack.

---

*Example*

```typescript
// After resolving, looks like
'arn:aws:cloudformation:us-west-2:123456789012:stack/teststack/51af3dc0-da77-11e4-872e-1234567db123'
```


##### `stackName`<sup>Required</sup> <a name="stackName" id="cdk-constructs.DockerBuildAndPush.property.stackName"></a>

```typescript
public readonly stackName: string;
```

- *Type:* string

The concrete CloudFormation physical stack name.

This is either the name defined explicitly in the `stackName` prop or
allocated based on the stack's location in the construct tree. Stacks that
are directly defined under the app use their construct `id` as their stack
name. Stacks that are defined deeper within the tree will use a hashed naming
scheme based on the construct path to ensure uniqueness.

If you wish to obtain the deploy-time AWS::StackName intrinsic,
you can use `Aws.STACK_NAME` directly.

---

##### `synthesizer`<sup>Required</sup> <a name="synthesizer" id="cdk-constructs.DockerBuildAndPush.property.synthesizer"></a>

```typescript
public readonly synthesizer: IStackSynthesizer;
```

- *Type:* aws-cdk-lib.IStackSynthesizer

Synthesis method for this stack.

---

##### `tags`<sup>Required</sup> <a name="tags" id="cdk-constructs.DockerBuildAndPush.property.tags"></a>

```typescript
public readonly tags: TagManager;
```

- *Type:* aws-cdk-lib.TagManager

Tags to be applied to the stack.

---

##### `templateFile`<sup>Required</sup> <a name="templateFile" id="cdk-constructs.DockerBuildAndPush.property.templateFile"></a>

```typescript
public readonly templateFile: string;
```

- *Type:* string

The name of the CloudFormation template file emitted to the output directory during synthesis.

Example value: `MyStack.template.json`

---

##### `templateOptions`<sup>Required</sup> <a name="templateOptions" id="cdk-constructs.DockerBuildAndPush.property.templateOptions"></a>

```typescript
public readonly templateOptions: ITemplateOptions;
```

- *Type:* aws-cdk-lib.ITemplateOptions

Options for CloudFormation template (like version, transform, description).

---

##### `urlSuffix`<sup>Required</sup> <a name="urlSuffix" id="cdk-constructs.DockerBuildAndPush.property.urlSuffix"></a>

```typescript
public readonly urlSuffix: string;
```

- *Type:* string

The Amazon domain suffix for the region in which this stack is defined.

---

##### `nestedStackParent`<sup>Optional</sup> <a name="nestedStackParent" id="cdk-constructs.DockerBuildAndPush.property.nestedStackParent"></a>

```typescript
public readonly nestedStackParent: Stack;
```

- *Type:* aws-cdk-lib.Stack

If this is a nested stack, returns it's parent stack.

---

##### `nestedStackResource`<sup>Optional</sup> <a name="nestedStackResource" id="cdk-constructs.DockerBuildAndPush.property.nestedStackResource"></a>

```typescript
public readonly nestedStackResource: CfnResource;
```

- *Type:* aws-cdk-lib.CfnResource

If this is a nested stack, this represents its `AWS::CloudFormation::Stack` resource.

`undefined` for top-level (non-nested) stacks.

---

##### `terminationProtection`<sup>Required</sup> <a name="terminationProtection" id="cdk-constructs.DockerBuildAndPush.property.terminationProtection"></a>

```typescript
public readonly terminationProtection: boolean;
```

- *Type:* boolean

Whether termination protection is enabled for this stack.

---

##### `ecrImage`<sup>Required</sup> <a name="ecrImage" id="cdk-constructs.DockerBuildAndPush.property.ecrImage"></a>

```typescript
public readonly ecrImage: EcrImage;
```

- *Type:* aws-cdk-lib.aws_ecs.EcrImage

---

##### `lambdaDockerImageCode`<sup>Required</sup> <a name="lambdaDockerImageCode" id="cdk-constructs.DockerBuildAndPush.property.lambdaDockerImageCode"></a>

```typescript
public readonly lambdaDockerImageCode: DockerImageCode;
```

- *Type:* aws-cdk-lib.aws_lambda.DockerImageCode

---


### ECRDeployment <a name="ECRDeployment" id="cdk-constructs.ECRDeployment"></a>

#### Initializers <a name="Initializers" id="cdk-constructs.ECRDeployment.Initializer"></a>

```typescript
import { ECRDeployment } from 'cdk-constructs'

new ECRDeployment(scope: Construct, id: string, props: ECRDeploymentProps)
```

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.ECRDeployment.Initializer.parameter.scope">scope</a></code> | <code>constructs.Construct</code> | *No description.* |
| <code><a href="#cdk-constructs.ECRDeployment.Initializer.parameter.id">id</a></code> | <code>string</code> | *No description.* |
| <code><a href="#cdk-constructs.ECRDeployment.Initializer.parameter.props">props</a></code> | <code><a href="#cdk-constructs.ECRDeploymentProps">ECRDeploymentProps</a></code> | *No description.* |

---

##### `scope`<sup>Required</sup> <a name="scope" id="cdk-constructs.ECRDeployment.Initializer.parameter.scope"></a>

- *Type:* constructs.Construct

---

##### `id`<sup>Required</sup> <a name="id" id="cdk-constructs.ECRDeployment.Initializer.parameter.id"></a>

- *Type:* string

---

##### `props`<sup>Required</sup> <a name="props" id="cdk-constructs.ECRDeployment.Initializer.parameter.props"></a>

- *Type:* <a href="#cdk-constructs.ECRDeploymentProps">ECRDeploymentProps</a>

---

#### Methods <a name="Methods" id="Methods"></a>

| **Name** | **Description** |
| --- | --- |
| <code><a href="#cdk-constructs.ECRDeployment.toString">toString</a></code> | Returns a string representation of this construct. |
| <code><a href="#cdk-constructs.ECRDeployment.addToPrincipalPolicy">addToPrincipalPolicy</a></code> | *No description.* |

---

##### `toString` <a name="toString" id="cdk-constructs.ECRDeployment.toString"></a>

```typescript
public toString(): string
```

Returns a string representation of this construct.

##### `addToPrincipalPolicy` <a name="addToPrincipalPolicy" id="cdk-constructs.ECRDeployment.addToPrincipalPolicy"></a>

```typescript
public addToPrincipalPolicy(statement: PolicyStatement): AddToPrincipalPolicyResult
```

###### `statement`<sup>Required</sup> <a name="statement" id="cdk-constructs.ECRDeployment.addToPrincipalPolicy.parameter.statement"></a>

- *Type:* aws-cdk-lib.aws_iam.PolicyStatement

---

#### Static Functions <a name="Static Functions" id="Static Functions"></a>

| **Name** | **Description** |
| --- | --- |
| <code><a href="#cdk-constructs.ECRDeployment.isConstruct">isConstruct</a></code> | Checks if `x` is a construct. |

---

##### `isConstruct` <a name="isConstruct" id="cdk-constructs.ECRDeployment.isConstruct"></a>

```typescript
import { ECRDeployment } from 'cdk-constructs'

ECRDeployment.isConstruct(x: any)
```

Checks if `x` is a construct.

Use this method instead of `instanceof` to properly detect `Construct`
instances, even when the construct library is symlinked.

Explanation: in JavaScript, multiple copies of the `constructs` library on
disk are seen as independent, completely different libraries. As a
consequence, the class `Construct` in each copy of the `constructs` library
is seen as a different class, and an instance of one class will not test as
`instanceof` the other class. `npm install` will not create installations
like this, but users may manually symlink construct libraries together or
use a monorepo tool: in those cases, multiple copies of the `constructs`
library can be accidentally installed, and `instanceof` will behave
unpredictably. It is safest to avoid using `instanceof`, and using
this type-testing method instead.

###### `x`<sup>Required</sup> <a name="x" id="cdk-constructs.ECRDeployment.isConstruct.parameter.x"></a>

- *Type:* any

Any object.

---

#### Properties <a name="Properties" id="Properties"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.ECRDeployment.property.node">node</a></code> | <code>constructs.Node</code> | The tree node. |

---

##### `node`<sup>Required</sup> <a name="node" id="cdk-constructs.ECRDeployment.property.node"></a>

```typescript
public readonly node: Node;
```

- *Type:* constructs.Node

The tree node.

---


### EndpointAlb <a name="EndpointAlb" id="cdk-constructs.EndpointAlb"></a>

#### Methods <a name="Methods" id="Methods"></a>

| **Name** | **Description** |
| --- | --- |
| <code><a href="#cdk-constructs.EndpointAlb.toString">toString</a></code> | Returns a string representation of this construct. |
| <code><a href="#cdk-constructs.EndpointAlb.buildTGConditions">buildTGConditions</a></code> | Build ALB Listener routing condition based on routing token and service name. |
| <code><a href="#cdk-constructs.EndpointAlb.withTarget">withTarget</a></code> | Set the target of the endpoint. |

---

##### `toString` <a name="toString" id="cdk-constructs.EndpointAlb.toString"></a>

```typescript
public toString(): string
```

Returns a string representation of this construct.

##### `buildTGConditions` <a name="buildTGConditions" id="cdk-constructs.EndpointAlb.buildTGConditions"></a>

```typescript
public buildTGConditions(serviceName: string, routingTokenPrefix: string, serviceGroup: string): ListenerCondition[]
```

Build ALB Listener routing condition based on routing token and service name.

###### `serviceName`<sup>Required</sup> <a name="serviceName" id="cdk-constructs.EndpointAlb.buildTGConditions.parameter.serviceName"></a>

- *Type:* string

service name.

---

###### `routingTokenPrefix`<sup>Required</sup> <a name="routingTokenPrefix" id="cdk-constructs.EndpointAlb.buildTGConditions.parameter.routingTokenPrefix"></a>

- *Type:* string

routing token.

---

###### `serviceGroup`<sup>Required</sup> <a name="serviceGroup" id="cdk-constructs.EndpointAlb.buildTGConditions.parameter.serviceGroup"></a>

- *Type:* string

---

##### `withTarget` <a name="withTarget" id="cdk-constructs.EndpointAlb.withTarget"></a>

```typescript
public withTarget(targetGroup: ApplicationTargetGroup): EndpointAlb
```

Set the target of the endpoint.

###### `targetGroup`<sup>Required</sup> <a name="targetGroup" id="cdk-constructs.EndpointAlb.withTarget.parameter.targetGroup"></a>

- *Type:* aws-cdk-lib.aws_elasticloadbalancingv2.ApplicationTargetGroup

---

#### Static Functions <a name="Static Functions" id="Static Functions"></a>

| **Name** | **Description** |
| --- | --- |
| <code><a href="#cdk-constructs.EndpointAlb.isConstruct">isConstruct</a></code> | Checks if `x` is a construct. |
| <code><a href="#cdk-constructs.EndpointAlb.legacyEndpoint">legacyEndpoint</a></code> | Build an endpoint without any validation on path prefix. |
| <code><a href="#cdk-constructs.EndpointAlb.thronEndpoint">thronEndpoint</a></code> | Build an endpoint using thron's conventions on path prefix. |

---

##### `isConstruct` <a name="isConstruct" id="cdk-constructs.EndpointAlb.isConstruct"></a>

```typescript
import { EndpointAlb } from 'cdk-constructs'

EndpointAlb.isConstruct(x: any)
```

Checks if `x` is a construct.

Use this method instead of `instanceof` to properly detect `Construct`
instances, even when the construct library is symlinked.

Explanation: in JavaScript, multiple copies of the `constructs` library on
disk are seen as independent, completely different libraries. As a
consequence, the class `Construct` in each copy of the `constructs` library
is seen as a different class, and an instance of one class will not test as
`instanceof` the other class. `npm install` will not create installations
like this, but users may manually symlink construct libraries together or
use a monorepo tool: in those cases, multiple copies of the `constructs`
library can be accidentally installed, and `instanceof` will behave
unpredictably. It is safest to avoid using `instanceof`, and using
this type-testing method instead.

###### `x`<sup>Required</sup> <a name="x" id="cdk-constructs.EndpointAlb.isConstruct.parameter.x"></a>

- *Type:* any

Any object.

---

##### `legacyEndpoint` <a name="legacyEndpoint" id="cdk-constructs.EndpointAlb.legacyEndpoint"></a>

```typescript
import { EndpointAlb } from 'cdk-constructs'

EndpointAlb.legacyEndpoint(scope: Construct, id: string, props: LegacyEndpointAlbProps)
```

Build an endpoint without any validation on path prefix.

###### `scope`<sup>Required</sup> <a name="scope" id="cdk-constructs.EndpointAlb.legacyEndpoint.parameter.scope"></a>

- *Type:* constructs.Construct

---

###### `id`<sup>Required</sup> <a name="id" id="cdk-constructs.EndpointAlb.legacyEndpoint.parameter.id"></a>

- *Type:* string

---

###### `props`<sup>Required</sup> <a name="props" id="cdk-constructs.EndpointAlb.legacyEndpoint.parameter.props"></a>

- *Type:* <a href="#cdk-constructs.LegacyEndpointAlbProps">LegacyEndpointAlbProps</a>

---

##### `thronEndpoint` <a name="thronEndpoint" id="cdk-constructs.EndpointAlb.thronEndpoint"></a>

```typescript
import { EndpointAlb } from 'cdk-constructs'

EndpointAlb.thronEndpoint(scope: Construct, id: string, props: ThronEndpointAlbProps)
```

Build an endpoint using thron's conventions on path prefix.

###### `scope`<sup>Required</sup> <a name="scope" id="cdk-constructs.EndpointAlb.thronEndpoint.parameter.scope"></a>

- *Type:* constructs.Construct

---

###### `id`<sup>Required</sup> <a name="id" id="cdk-constructs.EndpointAlb.thronEndpoint.parameter.id"></a>

- *Type:* string

---

###### `props`<sup>Required</sup> <a name="props" id="cdk-constructs.EndpointAlb.thronEndpoint.parameter.props"></a>

- *Type:* <a href="#cdk-constructs.ThronEndpointAlbProps">ThronEndpointAlbProps</a>

---

#### Properties <a name="Properties" id="Properties"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.EndpointAlb.property.node">node</a></code> | <code>constructs.Node</code> | The tree node. |
| <code><a href="#cdk-constructs.EndpointAlb.property.defaultValue">defaultValue</a></code> | <code><a href="#cdk-constructs.DefaultValue">DefaultValue</a></code> | Default Vaule class. |
| <code><a href="#cdk-constructs.EndpointAlb.property.routingTokenPrefix">routingTokenPrefix</a></code> | <code>string</code> | Routing path, validated against selected `serviceGroup` conventions. |
| <code><a href="#cdk-constructs.EndpointAlb.property.serviceGroup">serviceGroup</a></code> | <code><a href="#cdk-constructs.ServiceGroup">ServiceGroup</a></code> | Service group. |
| <code><a href="#cdk-constructs.EndpointAlb.property.sitename">sitename</a></code> | <code>string</code> | Sitename where the construct is being deployed. |
| <code><a href="#cdk-constructs.EndpointAlb.property.listener">listener</a></code> | <code>aws-cdk-lib.aws_elasticloadbalancingv2.IApplicationListener</code> | ALB Listener where the endpoint is attached. |
| <code><a href="#cdk-constructs.EndpointAlb.property.rulePriority">rulePriority</a></code> | <code>aws-cdk-lib.Reference</code> | ALB Listener Rule priority used for this endpoint. |
| <code><a href="#cdk-constructs.EndpointAlb.property.serviceName">serviceName</a></code> | <code>string</code> | Name of the service (generated). |
| <code><a href="#cdk-constructs.EndpointAlb.property.stack">stack</a></code> | <code>aws-cdk-lib.Stack</code> | The reference of parent Stack. |
| <code><a href="#cdk-constructs.EndpointAlb.property.version">version</a></code> | <code>number</code> | Version of the endpoint (available only on thronEndpoints). |
| <code><a href="#cdk-constructs.EndpointAlb.property.visibility">visibility</a></code> | <code><a href="#cdk-constructs.EndpointVisibility">EndpointVisibility</a></code> | Visibility of the endpint (available only on thronEndpoints). |

---

##### `node`<sup>Required</sup> <a name="node" id="cdk-constructs.EndpointAlb.property.node"></a>

```typescript
public readonly node: Node;
```

- *Type:* constructs.Node

The tree node.

---

##### `defaultValue`<sup>Required</sup> <a name="defaultValue" id="cdk-constructs.EndpointAlb.property.defaultValue"></a>

```typescript
public readonly defaultValue: DefaultValue;
```

- *Type:* <a href="#cdk-constructs.DefaultValue">DefaultValue</a>

Default Vaule class.

---

##### `routingTokenPrefix`<sup>Required</sup> <a name="routingTokenPrefix" id="cdk-constructs.EndpointAlb.property.routingTokenPrefix"></a>

```typescript
public readonly routingTokenPrefix: string;
```

- *Type:* string

Routing path, validated against selected `serviceGroup` conventions.

---

##### `serviceGroup`<sup>Required</sup> <a name="serviceGroup" id="cdk-constructs.EndpointAlb.property.serviceGroup"></a>

```typescript
public readonly serviceGroup: ServiceGroup;
```

- *Type:* <a href="#cdk-constructs.ServiceGroup">ServiceGroup</a>

Service group.

---

##### `sitename`<sup>Required</sup> <a name="sitename" id="cdk-constructs.EndpointAlb.property.sitename"></a>

```typescript
public readonly sitename: string;
```

- *Type:* string

Sitename where the construct is being deployed.

---

##### `listener`<sup>Optional</sup> <a name="listener" id="cdk-constructs.EndpointAlb.property.listener"></a>

```typescript
public readonly listener: IApplicationListener;
```

- *Type:* aws-cdk-lib.aws_elasticloadbalancingv2.IApplicationListener

ALB Listener where the endpoint is attached.

---

##### `rulePriority`<sup>Optional</sup> <a name="rulePriority" id="cdk-constructs.EndpointAlb.property.rulePriority"></a>

```typescript
public readonly rulePriority: Reference;
```

- *Type:* aws-cdk-lib.Reference

ALB Listener Rule priority used for this endpoint.

---

##### `serviceName`<sup>Optional</sup> <a name="serviceName" id="cdk-constructs.EndpointAlb.property.serviceName"></a>

```typescript
public readonly serviceName: string;
```

- *Type:* string

Name of the service (generated).

---

##### `stack`<sup>Optional</sup> <a name="stack" id="cdk-constructs.EndpointAlb.property.stack"></a>

```typescript
public readonly stack: Stack;
```

- *Type:* aws-cdk-lib.Stack

The reference of parent Stack.

---

##### `version`<sup>Optional</sup> <a name="version" id="cdk-constructs.EndpointAlb.property.version"></a>

```typescript
public readonly version: number;
```

- *Type:* number

Version of the endpoint (available only on thronEndpoints).

---

##### `visibility`<sup>Optional</sup> <a name="visibility" id="cdk-constructs.EndpointAlb.property.visibility"></a>

```typescript
public readonly visibility: EndpointVisibility;
```

- *Type:* <a href="#cdk-constructs.EndpointVisibility">EndpointVisibility</a>

Visibility of the endpint (available only on thronEndpoints).

---


### SsmParameterReader <a name="SsmParameterReader" id="cdk-constructs.SsmParameterReader"></a>

Class instantiating the SSMParameterReader custom resources, which allows you to read encrypted ssm parameters and use them as input for other constructs, i.e. lambda environment.

*Example*

```typescript
 const ssmParameterValue: string = new SsmParameterReader(this, 'example-id',{
   parameterName: "/example/param"
 }).stringValue;
```


#### Initializers <a name="Initializers" id="cdk-constructs.SsmParameterReader.Initializer"></a>

```typescript
import { SsmParameterReader } from 'cdk-constructs'

new SsmParameterReader(scope: Construct, id: string, props: SsmParameterReaderProps)
```

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.SsmParameterReader.Initializer.parameter.scope">scope</a></code> | <code>constructs.Construct</code> | *No description.* |
| <code><a href="#cdk-constructs.SsmParameterReader.Initializer.parameter.id">id</a></code> | <code>string</code> | *No description.* |
| <code><a href="#cdk-constructs.SsmParameterReader.Initializer.parameter.props">props</a></code> | <code><a href="#cdk-constructs.SsmParameterReaderProps">SsmParameterReaderProps</a></code> | *No description.* |

---

##### `scope`<sup>Required</sup> <a name="scope" id="cdk-constructs.SsmParameterReader.Initializer.parameter.scope"></a>

- *Type:* constructs.Construct

---

##### `id`<sup>Required</sup> <a name="id" id="cdk-constructs.SsmParameterReader.Initializer.parameter.id"></a>

- *Type:* string

---

##### `props`<sup>Required</sup> <a name="props" id="cdk-constructs.SsmParameterReader.Initializer.parameter.props"></a>

- *Type:* <a href="#cdk-constructs.SsmParameterReaderProps">SsmParameterReaderProps</a>

---

#### Methods <a name="Methods" id="Methods"></a>

| **Name** | **Description** |
| --- | --- |
| <code><a href="#cdk-constructs.SsmParameterReader.toString">toString</a></code> | Returns a string representation of this construct. |

---

##### `toString` <a name="toString" id="cdk-constructs.SsmParameterReader.toString"></a>

```typescript
public toString(): string
```

Returns a string representation of this construct.

#### Static Functions <a name="Static Functions" id="Static Functions"></a>

| **Name** | **Description** |
| --- | --- |
| <code><a href="#cdk-constructs.SsmParameterReader.isConstruct">isConstruct</a></code> | Checks if `x` is a construct. |

---

##### `isConstruct` <a name="isConstruct" id="cdk-constructs.SsmParameterReader.isConstruct"></a>

```typescript
import { SsmParameterReader } from 'cdk-constructs'

SsmParameterReader.isConstruct(x: any)
```

Checks if `x` is a construct.

Use this method instead of `instanceof` to properly detect `Construct`
instances, even when the construct library is symlinked.

Explanation: in JavaScript, multiple copies of the `constructs` library on
disk are seen as independent, completely different libraries. As a
consequence, the class `Construct` in each copy of the `constructs` library
is seen as a different class, and an instance of one class will not test as
`instanceof` the other class. `npm install` will not create installations
like this, but users may manually symlink construct libraries together or
use a monorepo tool: in those cases, multiple copies of the `constructs`
library can be accidentally installed, and `instanceof` will behave
unpredictably. It is safest to avoid using `instanceof`, and using
this type-testing method instead.

###### `x`<sup>Required</sup> <a name="x" id="cdk-constructs.SsmParameterReader.isConstruct.parameter.x"></a>

- *Type:* any

Any object.

---

#### Properties <a name="Properties" id="Properties"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.SsmParameterReader.property.node">node</a></code> | <code>constructs.Node</code> | The tree node. |
| <code><a href="#cdk-constructs.SsmParameterReader.property.stringValue">stringValue</a></code> | <code>string</code> | Unencrypted Value of the SSM Parameter. |

---

##### `node`<sup>Required</sup> <a name="node" id="cdk-constructs.SsmParameterReader.property.node"></a>

```typescript
public readonly node: Node;
```

- *Type:* constructs.Node

The tree node.

---

##### `stringValue`<sup>Required</sup> <a name="stringValue" id="cdk-constructs.SsmParameterReader.property.stringValue"></a>

```typescript
public readonly stringValue: string;
```

- *Type:* string

Unencrypted Value of the SSM Parameter.

---


### ThronAcmCertificate <a name="ThronAcmCertificate" id="cdk-constructs.ThronAcmCertificate"></a>

#### Initializers <a name="Initializers" id="cdk-constructs.ThronAcmCertificate.Initializer"></a>

```typescript
import { ThronAcmCertificate } from 'cdk-constructs'

new ThronAcmCertificate(scope: Stack, id: string, props: ThronAcmCertificateProps)
```

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.ThronAcmCertificate.Initializer.parameter.scope">scope</a></code> | <code>aws-cdk-lib.Stack</code> | *No description.* |
| <code><a href="#cdk-constructs.ThronAcmCertificate.Initializer.parameter.id">id</a></code> | <code>string</code> | *No description.* |
| <code><a href="#cdk-constructs.ThronAcmCertificate.Initializer.parameter.props">props</a></code> | <code><a href="#cdk-constructs.ThronAcmCertificateProps">ThronAcmCertificateProps</a></code> | *No description.* |

---

##### `scope`<sup>Required</sup> <a name="scope" id="cdk-constructs.ThronAcmCertificate.Initializer.parameter.scope"></a>

- *Type:* aws-cdk-lib.Stack

---

##### `id`<sup>Required</sup> <a name="id" id="cdk-constructs.ThronAcmCertificate.Initializer.parameter.id"></a>

- *Type:* string

---

##### `props`<sup>Required</sup> <a name="props" id="cdk-constructs.ThronAcmCertificate.Initializer.parameter.props"></a>

- *Type:* <a href="#cdk-constructs.ThronAcmCertificateProps">ThronAcmCertificateProps</a>

---

#### Methods <a name="Methods" id="Methods"></a>

| **Name** | **Description** |
| --- | --- |
| <code><a href="#cdk-constructs.ThronAcmCertificate.toString">toString</a></code> | Returns a string representation of this construct. |
| <code><a href="#cdk-constructs.ThronAcmCertificate.addDependency">addDependency</a></code> | Add a dependency between this stack and another stack. |
| <code><a href="#cdk-constructs.ThronAcmCertificate.addMetadata">addMetadata</a></code> | Adds an arbitrary key-value pair, with information you want to record about the stack. |
| <code><a href="#cdk-constructs.ThronAcmCertificate.addTransform">addTransform</a></code> | Add a Transform to this stack. A Transform is a macro that AWS CloudFormation uses to process your template. |
| <code><a href="#cdk-constructs.ThronAcmCertificate.exportStringListValue">exportStringListValue</a></code> | Create a CloudFormation Export for a string list value. |
| <code><a href="#cdk-constructs.ThronAcmCertificate.exportValue">exportValue</a></code> | Create a CloudFormation Export for a string value. |
| <code><a href="#cdk-constructs.ThronAcmCertificate.formatArn">formatArn</a></code> | Creates an ARN from components. |
| <code><a href="#cdk-constructs.ThronAcmCertificate.getLogicalId">getLogicalId</a></code> | Allocates a stack-unique CloudFormation-compatible logical identity for a specific resource. |
| <code><a href="#cdk-constructs.ThronAcmCertificate.regionalFact">regionalFact</a></code> | Look up a fact value for the given fact for the region of this stack. |
| <code><a href="#cdk-constructs.ThronAcmCertificate.renameLogicalId">renameLogicalId</a></code> | Rename a generated logical identities. |
| <code><a href="#cdk-constructs.ThronAcmCertificate.reportMissingContextKey">reportMissingContextKey</a></code> | Indicate that a context key was expected. |
| <code><a href="#cdk-constructs.ThronAcmCertificate.resolve">resolve</a></code> | Resolve a tokenized value in the context of the current stack. |
| <code><a href="#cdk-constructs.ThronAcmCertificate.splitArn">splitArn</a></code> | Splits the provided ARN into its components. |
| <code><a href="#cdk-constructs.ThronAcmCertificate.toJsonString">toJsonString</a></code> | Convert an object, potentially containing tokens, to a JSON string. |
| <code><a href="#cdk-constructs.ThronAcmCertificate.toYamlString">toYamlString</a></code> | Convert an object, potentially containing tokens, to a YAML string. |

---

##### `toString` <a name="toString" id="cdk-constructs.ThronAcmCertificate.toString"></a>

```typescript
public toString(): string
```

Returns a string representation of this construct.

##### `addDependency` <a name="addDependency" id="cdk-constructs.ThronAcmCertificate.addDependency"></a>

```typescript
public addDependency(target: Stack, reason?: string): void
```

Add a dependency between this stack and another stack.

This can be used to define dependencies between any two stacks within an
app, and also supports nested stacks.

###### `target`<sup>Required</sup> <a name="target" id="cdk-constructs.ThronAcmCertificate.addDependency.parameter.target"></a>

- *Type:* aws-cdk-lib.Stack

---

###### `reason`<sup>Optional</sup> <a name="reason" id="cdk-constructs.ThronAcmCertificate.addDependency.parameter.reason"></a>

- *Type:* string

---

##### `addMetadata` <a name="addMetadata" id="cdk-constructs.ThronAcmCertificate.addMetadata"></a>

```typescript
public addMetadata(key: string, value: any): void
```

Adds an arbitrary key-value pair, with information you want to record about the stack.

These get translated to the Metadata section of the generated template.

> [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/metadata-section-structure.html](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/metadata-section-structure.html)

###### `key`<sup>Required</sup> <a name="key" id="cdk-constructs.ThronAcmCertificate.addMetadata.parameter.key"></a>

- *Type:* string

---

###### `value`<sup>Required</sup> <a name="value" id="cdk-constructs.ThronAcmCertificate.addMetadata.parameter.value"></a>

- *Type:* any

---

##### `addTransform` <a name="addTransform" id="cdk-constructs.ThronAcmCertificate.addTransform"></a>

```typescript
public addTransform(transform: string): void
```

Add a Transform to this stack. A Transform is a macro that AWS CloudFormation uses to process your template.

Duplicate values are removed when stack is synthesized.

> [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/transform-section-structure.html](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/transform-section-structure.html)

*Example*

```typescript
declare const stack: Stack;

stack.addTransform('AWS::Serverless-2016-10-31')
```


###### `transform`<sup>Required</sup> <a name="transform" id="cdk-constructs.ThronAcmCertificate.addTransform.parameter.transform"></a>

- *Type:* string

The transform to add.

---

##### `exportStringListValue` <a name="exportStringListValue" id="cdk-constructs.ThronAcmCertificate.exportStringListValue"></a>

```typescript
public exportStringListValue(exportedValue: any, options?: ExportValueOptions): string[]
```

Create a CloudFormation Export for a string list value.

Returns a string list representing the corresponding `Fn.importValue()`
expression for this Export. The export expression is automatically wrapped with an
`Fn::Join` and the import value with an `Fn::Split`, since CloudFormation can only
export strings. You can control the name for the export by passing the `name` option.

If you don't supply a value for `name`, the value you're exporting must be
a Resource attribute (for example: `bucket.bucketName`) and it will be
given the same name as the automatic cross-stack reference that would be created
if you used the attribute in another Stack.

One of the uses for this method is to *remove* the relationship between
two Stacks established by automatic cross-stack references. It will
temporarily ensure that the CloudFormation Export still exists while you
remove the reference from the consuming stack. After that, you can remove
the resource and the manual export.

See `exportValue` for an example of this process.

###### `exportedValue`<sup>Required</sup> <a name="exportedValue" id="cdk-constructs.ThronAcmCertificate.exportStringListValue.parameter.exportedValue"></a>

- *Type:* any

---

###### `options`<sup>Optional</sup> <a name="options" id="cdk-constructs.ThronAcmCertificate.exportStringListValue.parameter.options"></a>

- *Type:* aws-cdk-lib.ExportValueOptions

---

##### `exportValue` <a name="exportValue" id="cdk-constructs.ThronAcmCertificate.exportValue"></a>

```typescript
public exportValue(exportedValue: any, options?: ExportValueOptions): string
```

Create a CloudFormation Export for a string value.

Returns a string representing the corresponding `Fn.importValue()`
expression for this Export. You can control the name for the export by
passing the `name` option.

If you don't supply a value for `name`, the value you're exporting must be
a Resource attribute (for example: `bucket.bucketName`) and it will be
given the same name as the automatic cross-stack reference that would be created
if you used the attribute in another Stack.

One of the uses for this method is to *remove* the relationship between
two Stacks established by automatic cross-stack references. It will
temporarily ensure that the CloudFormation Export still exists while you
remove the reference from the consuming stack. After that, you can remove
the resource and the manual export.

Here is how the process works. Let's say there are two stacks,
`producerStack` and `consumerStack`, and `producerStack` has a bucket
called `bucket`, which is referenced by `consumerStack` (perhaps because
an AWS Lambda Function writes into it, or something like that).

It is not safe to remove `producerStack.bucket` because as the bucket is being
deleted, `consumerStack` might still be using it.

Instead, the process takes two deployments:

**Deployment 1: break the relationship**:

- Make sure `consumerStack` no longer references `bucket.bucketName` (maybe the consumer
  stack now uses its own bucket, or it writes to an AWS DynamoDB table, or maybe you just
  remove the Lambda Function altogether).
- In the `ProducerStack` class, call `this.exportValue(this.bucket.bucketName)`. This
  will make sure the CloudFormation Export continues to exist while the relationship
  between the two stacks is being broken.
- Deploy (this will effectively only change the `consumerStack`, but it's safe to deploy both).

**Deployment 2: remove the bucket resource**:

- You are now free to remove the `bucket` resource from `producerStack`.
- Don't forget to remove the `exportValue()` call as well.
- Deploy again (this time only the `producerStack` will be changed -- the bucket will be deleted).

###### `exportedValue`<sup>Required</sup> <a name="exportedValue" id="cdk-constructs.ThronAcmCertificate.exportValue.parameter.exportedValue"></a>

- *Type:* any

---

###### `options`<sup>Optional</sup> <a name="options" id="cdk-constructs.ThronAcmCertificate.exportValue.parameter.options"></a>

- *Type:* aws-cdk-lib.ExportValueOptions

---

##### `formatArn` <a name="formatArn" id="cdk-constructs.ThronAcmCertificate.formatArn"></a>

```typescript
public formatArn(components: ArnComponents): string
```

Creates an ARN from components.

If `partition`, `region` or `account` are not specified, the stack's
partition, region and account will be used.

If any component is the empty string, an empty string will be inserted
into the generated ARN at the location that component corresponds to.

The ARN will be formatted as follows:

  arn:{partition}:{service}:{region}:{account}:{resource}{sep}{resource-name}

The required ARN pieces that are omitted will be taken from the stack that
the 'scope' is attached to. If all ARN pieces are supplied, the supplied scope
can be 'undefined'.

###### `components`<sup>Required</sup> <a name="components" id="cdk-constructs.ThronAcmCertificate.formatArn.parameter.components"></a>

- *Type:* aws-cdk-lib.ArnComponents

---

##### `getLogicalId` <a name="getLogicalId" id="cdk-constructs.ThronAcmCertificate.getLogicalId"></a>

```typescript
public getLogicalId(element: CfnElement): string
```

Allocates a stack-unique CloudFormation-compatible logical identity for a specific resource.

This method is called when a `CfnElement` is created and used to render the
initial logical identity of resources. Logical ID renames are applied at
this stage.

This method uses the protected method `allocateLogicalId` to render the
logical ID for an element. To modify the naming scheme, extend the `Stack`
class and override this method.

###### `element`<sup>Required</sup> <a name="element" id="cdk-constructs.ThronAcmCertificate.getLogicalId.parameter.element"></a>

- *Type:* aws-cdk-lib.CfnElement

The CloudFormation element for which a logical identity is needed.

---

##### `regionalFact` <a name="regionalFact" id="cdk-constructs.ThronAcmCertificate.regionalFact"></a>

```typescript
public regionalFact(factName: string, defaultValue?: string): string
```

Look up a fact value for the given fact for the region of this stack.

Will return a definite value only if the region of the current stack is resolved.
If not, a lookup map will be added to the stack and the lookup will be done at
CDK deployment time.

What regions will be included in the lookup map is controlled by the
`@aws-cdk/core:target-partitions` context value: it must be set to a list
of partitions, and only regions from the given partitions will be included.
If no such context key is set, all regions will be included.

This function is intended to be used by construct library authors. Application
builders can rely on the abstractions offered by construct libraries and do
not have to worry about regional facts.

If `defaultValue` is not given, it is an error if the fact is unknown for
the given region.

###### `factName`<sup>Required</sup> <a name="factName" id="cdk-constructs.ThronAcmCertificate.regionalFact.parameter.factName"></a>

- *Type:* string

---

###### `defaultValue`<sup>Optional</sup> <a name="defaultValue" id="cdk-constructs.ThronAcmCertificate.regionalFact.parameter.defaultValue"></a>

- *Type:* string

---

##### `renameLogicalId` <a name="renameLogicalId" id="cdk-constructs.ThronAcmCertificate.renameLogicalId"></a>

```typescript
public renameLogicalId(oldId: string, newId: string): void
```

Rename a generated logical identities.

To modify the naming scheme strategy, extend the `Stack` class and
override the `allocateLogicalId` method.

###### `oldId`<sup>Required</sup> <a name="oldId" id="cdk-constructs.ThronAcmCertificate.renameLogicalId.parameter.oldId"></a>

- *Type:* string

---

###### `newId`<sup>Required</sup> <a name="newId" id="cdk-constructs.ThronAcmCertificate.renameLogicalId.parameter.newId"></a>

- *Type:* string

---

##### `reportMissingContextKey` <a name="reportMissingContextKey" id="cdk-constructs.ThronAcmCertificate.reportMissingContextKey"></a>

```typescript
public reportMissingContextKey(report: MissingContext): void
```

Indicate that a context key was expected.

Contains instructions which will be emitted into the cloud assembly on how
the key should be supplied.

###### `report`<sup>Required</sup> <a name="report" id="cdk-constructs.ThronAcmCertificate.reportMissingContextKey.parameter.report"></a>

- *Type:* aws-cdk-lib.cloud_assembly_schema.MissingContext

The set of parameters needed to obtain the context.

---

##### `resolve` <a name="resolve" id="cdk-constructs.ThronAcmCertificate.resolve"></a>

```typescript
public resolve(obj: any): any
```

Resolve a tokenized value in the context of the current stack.

###### `obj`<sup>Required</sup> <a name="obj" id="cdk-constructs.ThronAcmCertificate.resolve.parameter.obj"></a>

- *Type:* any

---

##### `splitArn` <a name="splitArn" id="cdk-constructs.ThronAcmCertificate.splitArn"></a>

```typescript
public splitArn(arn: string, arnFormat: ArnFormat): ArnComponents
```

Splits the provided ARN into its components.

Works both if 'arn' is a string like 'arn:aws:s3:::bucket',
and a Token representing a dynamic CloudFormation expression
(in which case the returned components will also be dynamic CloudFormation expressions,
encoded as Tokens).

###### `arn`<sup>Required</sup> <a name="arn" id="cdk-constructs.ThronAcmCertificate.splitArn.parameter.arn"></a>

- *Type:* string

the ARN to split into its components.

---

###### `arnFormat`<sup>Required</sup> <a name="arnFormat" id="cdk-constructs.ThronAcmCertificate.splitArn.parameter.arnFormat"></a>

- *Type:* aws-cdk-lib.ArnFormat

the expected format of 'arn' - depends on what format the service 'arn' represents uses.

---

##### `toJsonString` <a name="toJsonString" id="cdk-constructs.ThronAcmCertificate.toJsonString"></a>

```typescript
public toJsonString(obj: any, space?: number): string
```

Convert an object, potentially containing tokens, to a JSON string.

###### `obj`<sup>Required</sup> <a name="obj" id="cdk-constructs.ThronAcmCertificate.toJsonString.parameter.obj"></a>

- *Type:* any

---

###### `space`<sup>Optional</sup> <a name="space" id="cdk-constructs.ThronAcmCertificate.toJsonString.parameter.space"></a>

- *Type:* number

---

##### `toYamlString` <a name="toYamlString" id="cdk-constructs.ThronAcmCertificate.toYamlString"></a>

```typescript
public toYamlString(obj: any): string
```

Convert an object, potentially containing tokens, to a YAML string.

###### `obj`<sup>Required</sup> <a name="obj" id="cdk-constructs.ThronAcmCertificate.toYamlString.parameter.obj"></a>

- *Type:* any

---

#### Static Functions <a name="Static Functions" id="Static Functions"></a>

| **Name** | **Description** |
| --- | --- |
| <code><a href="#cdk-constructs.ThronAcmCertificate.isConstruct">isConstruct</a></code> | Checks if `x` is a construct. |
| <code><a href="#cdk-constructs.ThronAcmCertificate.isStack">isStack</a></code> | Return whether the given object is a Stack. |
| <code><a href="#cdk-constructs.ThronAcmCertificate.of">of</a></code> | Looks up the first stack scope in which `construct` is defined. |

---

##### `isConstruct` <a name="isConstruct" id="cdk-constructs.ThronAcmCertificate.isConstruct"></a>

```typescript
import { ThronAcmCertificate } from 'cdk-constructs'

ThronAcmCertificate.isConstruct(x: any)
```

Checks if `x` is a construct.

Use this method instead of `instanceof` to properly detect `Construct`
instances, even when the construct library is symlinked.

Explanation: in JavaScript, multiple copies of the `constructs` library on
disk are seen as independent, completely different libraries. As a
consequence, the class `Construct` in each copy of the `constructs` library
is seen as a different class, and an instance of one class will not test as
`instanceof` the other class. `npm install` will not create installations
like this, but users may manually symlink construct libraries together or
use a monorepo tool: in those cases, multiple copies of the `constructs`
library can be accidentally installed, and `instanceof` will behave
unpredictably. It is safest to avoid using `instanceof`, and using
this type-testing method instead.

###### `x`<sup>Required</sup> <a name="x" id="cdk-constructs.ThronAcmCertificate.isConstruct.parameter.x"></a>

- *Type:* any

Any object.

---

##### `isStack` <a name="isStack" id="cdk-constructs.ThronAcmCertificate.isStack"></a>

```typescript
import { ThronAcmCertificate } from 'cdk-constructs'

ThronAcmCertificate.isStack(x: any)
```

Return whether the given object is a Stack.

We do attribute detection since we can't reliably use 'instanceof'.

###### `x`<sup>Required</sup> <a name="x" id="cdk-constructs.ThronAcmCertificate.isStack.parameter.x"></a>

- *Type:* any

---

##### `of` <a name="of" id="cdk-constructs.ThronAcmCertificate.of"></a>

```typescript
import { ThronAcmCertificate } from 'cdk-constructs'

ThronAcmCertificate.of(construct: IConstruct)
```

Looks up the first stack scope in which `construct` is defined.

Fails if there is no stack up the tree.

###### `construct`<sup>Required</sup> <a name="construct" id="cdk-constructs.ThronAcmCertificate.of.parameter.construct"></a>

- *Type:* constructs.IConstruct

The construct to start the search from.

---

#### Properties <a name="Properties" id="Properties"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.ThronAcmCertificate.property.node">node</a></code> | <code>constructs.Node</code> | The tree node. |
| <code><a href="#cdk-constructs.ThronAcmCertificate.property.account">account</a></code> | <code>string</code> | The AWS account into which this stack will be deployed. |
| <code><a href="#cdk-constructs.ThronAcmCertificate.property.artifactId">artifactId</a></code> | <code>string</code> | The ID of the cloud assembly artifact for this stack. |
| <code><a href="#cdk-constructs.ThronAcmCertificate.property.availabilityZones">availabilityZones</a></code> | <code>string[]</code> | Returns the list of AZs that are available in the AWS environment (account/region) associated with this stack. |
| <code><a href="#cdk-constructs.ThronAcmCertificate.property.bundlingRequired">bundlingRequired</a></code> | <code>boolean</code> | Indicates whether the stack requires bundling or not. |
| <code><a href="#cdk-constructs.ThronAcmCertificate.property.dependencies">dependencies</a></code> | <code>aws-cdk-lib.Stack[]</code> | Return the stacks this stack depends on. |
| <code><a href="#cdk-constructs.ThronAcmCertificate.property.environment">environment</a></code> | <code>string</code> | The environment coordinates in which this stack is deployed. |
| <code><a href="#cdk-constructs.ThronAcmCertificate.property.nested">nested</a></code> | <code>boolean</code> | Indicates if this is a nested stack, in which case `parentStack` will include a reference to it's parent. |
| <code><a href="#cdk-constructs.ThronAcmCertificate.property.notificationArns">notificationArns</a></code> | <code>string[]</code> | Returns the list of notification Amazon Resource Names (ARNs) for the current stack. |
| <code><a href="#cdk-constructs.ThronAcmCertificate.property.partition">partition</a></code> | <code>string</code> | The partition in which this stack is defined. |
| <code><a href="#cdk-constructs.ThronAcmCertificate.property.region">region</a></code> | <code>string</code> | The AWS region into which this stack will be deployed (e.g. `us-west-2`). |
| <code><a href="#cdk-constructs.ThronAcmCertificate.property.stackId">stackId</a></code> | <code>string</code> | The ID of the stack. |
| <code><a href="#cdk-constructs.ThronAcmCertificate.property.stackName">stackName</a></code> | <code>string</code> | The concrete CloudFormation physical stack name. |
| <code><a href="#cdk-constructs.ThronAcmCertificate.property.synthesizer">synthesizer</a></code> | <code>aws-cdk-lib.IStackSynthesizer</code> | Synthesis method for this stack. |
| <code><a href="#cdk-constructs.ThronAcmCertificate.property.tags">tags</a></code> | <code>aws-cdk-lib.TagManager</code> | Tags to be applied to the stack. |
| <code><a href="#cdk-constructs.ThronAcmCertificate.property.templateFile">templateFile</a></code> | <code>string</code> | The name of the CloudFormation template file emitted to the output directory during synthesis. |
| <code><a href="#cdk-constructs.ThronAcmCertificate.property.templateOptions">templateOptions</a></code> | <code>aws-cdk-lib.ITemplateOptions</code> | Options for CloudFormation template (like version, transform, description). |
| <code><a href="#cdk-constructs.ThronAcmCertificate.property.urlSuffix">urlSuffix</a></code> | <code>string</code> | The Amazon domain suffix for the region in which this stack is defined. |
| <code><a href="#cdk-constructs.ThronAcmCertificate.property.nestedStackParent">nestedStackParent</a></code> | <code>aws-cdk-lib.Stack</code> | If this is a nested stack, returns it's parent stack. |
| <code><a href="#cdk-constructs.ThronAcmCertificate.property.nestedStackResource">nestedStackResource</a></code> | <code>aws-cdk-lib.CfnResource</code> | If this is a nested stack, this represents its `AWS::CloudFormation::Stack` resource. |
| <code><a href="#cdk-constructs.ThronAcmCertificate.property.terminationProtection">terminationProtection</a></code> | <code>boolean</code> | Whether termination protection is enabled for this stack. |
| <code><a href="#cdk-constructs.ThronAcmCertificate.property.certificate">certificate</a></code> | <code>aws-cdk-lib.aws_certificatemanager.Certificate</code> | The issued certificate. |
| <code><a href="#cdk-constructs.ThronAcmCertificate.property.domainName">domainName</a></code> | <code>string</code> | FQDN the certificate is issued for. |
| <code><a href="#cdk-constructs.ThronAcmCertificate.property.subjectAlternativeNames">subjectAlternativeNames</a></code> | <code>string[]</code> | Alternative domain names on the certificate. |

---

##### `node`<sup>Required</sup> <a name="node" id="cdk-constructs.ThronAcmCertificate.property.node"></a>

```typescript
public readonly node: Node;
```

- *Type:* constructs.Node

The tree node.

---

##### `account`<sup>Required</sup> <a name="account" id="cdk-constructs.ThronAcmCertificate.property.account"></a>

```typescript
public readonly account: string;
```

- *Type:* string

The AWS account into which this stack will be deployed.

This value is resolved according to the following rules:

1. The value provided to `env.account` when the stack is defined. This can
   either be a concrete account (e.g. `585695031111`) or the
   `Aws.ACCOUNT_ID` token.
3. `Aws.ACCOUNT_ID`, which represents the CloudFormation intrinsic reference
   `{ "Ref": "AWS::AccountId" }` encoded as a string token.

Preferably, you should use the return value as an opaque string and not
attempt to parse it to implement your logic. If you do, you must first
check that it is a concrete value an not an unresolved token. If this
value is an unresolved token (`Token.isUnresolved(stack.account)` returns
`true`), this implies that the user wishes that this stack will synthesize
into an **account-agnostic template**. In this case, your code should either
fail (throw an error, emit a synth error using `Annotations.of(construct).addError()`) or
implement some other account-agnostic behavior.

---

##### `artifactId`<sup>Required</sup> <a name="artifactId" id="cdk-constructs.ThronAcmCertificate.property.artifactId"></a>

```typescript
public readonly artifactId: string;
```

- *Type:* string

The ID of the cloud assembly artifact for this stack.

---

##### `availabilityZones`<sup>Required</sup> <a name="availabilityZones" id="cdk-constructs.ThronAcmCertificate.property.availabilityZones"></a>

```typescript
public readonly availabilityZones: string[];
```

- *Type:* string[]

Returns the list of AZs that are available in the AWS environment (account/region) associated with this stack.

If the stack is environment-agnostic (either account and/or region are
tokens), this property will return an array with 2 tokens that will resolve
at deploy-time to the first two availability zones returned from CloudFormation's
`Fn::GetAZs` intrinsic function.

If they are not available in the context, returns a set of dummy values and
reports them as missing, and let the CLI resolve them by calling EC2
`DescribeAvailabilityZones` on the target environment.

To specify a different strategy for selecting availability zones override this method.

---

##### `bundlingRequired`<sup>Required</sup> <a name="bundlingRequired" id="cdk-constructs.ThronAcmCertificate.property.bundlingRequired"></a>

```typescript
public readonly bundlingRequired: boolean;
```

- *Type:* boolean

Indicates whether the stack requires bundling or not.

---

##### `dependencies`<sup>Required</sup> <a name="dependencies" id="cdk-constructs.ThronAcmCertificate.property.dependencies"></a>

```typescript
public readonly dependencies: Stack[];
```

- *Type:* aws-cdk-lib.Stack[]

Return the stacks this stack depends on.

---

##### `environment`<sup>Required</sup> <a name="environment" id="cdk-constructs.ThronAcmCertificate.property.environment"></a>

```typescript
public readonly environment: string;
```

- *Type:* string

The environment coordinates in which this stack is deployed.

In the form
`aws://account/region`. Use `stack.account` and `stack.region` to obtain
the specific values, no need to parse.

You can use this value to determine if two stacks are targeting the same
environment.

If either `stack.account` or `stack.region` are not concrete values (e.g.
`Aws.ACCOUNT_ID` or `Aws.REGION`) the special strings `unknown-account` and/or
`unknown-region` will be used respectively to indicate this stack is
region/account-agnostic.

---

##### `nested`<sup>Required</sup> <a name="nested" id="cdk-constructs.ThronAcmCertificate.property.nested"></a>

```typescript
public readonly nested: boolean;
```

- *Type:* boolean

Indicates if this is a nested stack, in which case `parentStack` will include a reference to it's parent.

---

##### `notificationArns`<sup>Required</sup> <a name="notificationArns" id="cdk-constructs.ThronAcmCertificate.property.notificationArns"></a>

```typescript
public readonly notificationArns: string[];
```

- *Type:* string[]

Returns the list of notification Amazon Resource Names (ARNs) for the current stack.

---

##### `partition`<sup>Required</sup> <a name="partition" id="cdk-constructs.ThronAcmCertificate.property.partition"></a>

```typescript
public readonly partition: string;
```

- *Type:* string

The partition in which this stack is defined.

---

##### `region`<sup>Required</sup> <a name="region" id="cdk-constructs.ThronAcmCertificate.property.region"></a>

```typescript
public readonly region: string;
```

- *Type:* string

The AWS region into which this stack will be deployed (e.g. `us-west-2`).

This value is resolved according to the following rules:

1. The value provided to `env.region` when the stack is defined. This can
   either be a concrete region (e.g. `us-west-2`) or the `Aws.REGION`
   token.
3. `Aws.REGION`, which is represents the CloudFormation intrinsic reference
   `{ "Ref": "AWS::Region" }` encoded as a string token.

Preferably, you should use the return value as an opaque string and not
attempt to parse it to implement your logic. If you do, you must first
check that it is a concrete value an not an unresolved token. If this
value is an unresolved token (`Token.isUnresolved(stack.region)` returns
`true`), this implies that the user wishes that this stack will synthesize
into a **region-agnostic template**. In this case, your code should either
fail (throw an error, emit a synth error using `Annotations.of(construct).addError()`) or
implement some other region-agnostic behavior.

---

##### `stackId`<sup>Required</sup> <a name="stackId" id="cdk-constructs.ThronAcmCertificate.property.stackId"></a>

```typescript
public readonly stackId: string;
```

- *Type:* string

The ID of the stack.

---

*Example*

```typescript
// After resolving, looks like
'arn:aws:cloudformation:us-west-2:123456789012:stack/teststack/51af3dc0-da77-11e4-872e-1234567db123'
```


##### `stackName`<sup>Required</sup> <a name="stackName" id="cdk-constructs.ThronAcmCertificate.property.stackName"></a>

```typescript
public readonly stackName: string;
```

- *Type:* string

The concrete CloudFormation physical stack name.

This is either the name defined explicitly in the `stackName` prop or
allocated based on the stack's location in the construct tree. Stacks that
are directly defined under the app use their construct `id` as their stack
name. Stacks that are defined deeper within the tree will use a hashed naming
scheme based on the construct path to ensure uniqueness.

If you wish to obtain the deploy-time AWS::StackName intrinsic,
you can use `Aws.STACK_NAME` directly.

---

##### `synthesizer`<sup>Required</sup> <a name="synthesizer" id="cdk-constructs.ThronAcmCertificate.property.synthesizer"></a>

```typescript
public readonly synthesizer: IStackSynthesizer;
```

- *Type:* aws-cdk-lib.IStackSynthesizer

Synthesis method for this stack.

---

##### `tags`<sup>Required</sup> <a name="tags" id="cdk-constructs.ThronAcmCertificate.property.tags"></a>

```typescript
public readonly tags: TagManager;
```

- *Type:* aws-cdk-lib.TagManager

Tags to be applied to the stack.

---

##### `templateFile`<sup>Required</sup> <a name="templateFile" id="cdk-constructs.ThronAcmCertificate.property.templateFile"></a>

```typescript
public readonly templateFile: string;
```

- *Type:* string

The name of the CloudFormation template file emitted to the output directory during synthesis.

Example value: `MyStack.template.json`

---

##### `templateOptions`<sup>Required</sup> <a name="templateOptions" id="cdk-constructs.ThronAcmCertificate.property.templateOptions"></a>

```typescript
public readonly templateOptions: ITemplateOptions;
```

- *Type:* aws-cdk-lib.ITemplateOptions

Options for CloudFormation template (like version, transform, description).

---

##### `urlSuffix`<sup>Required</sup> <a name="urlSuffix" id="cdk-constructs.ThronAcmCertificate.property.urlSuffix"></a>

```typescript
public readonly urlSuffix: string;
```

- *Type:* string

The Amazon domain suffix for the region in which this stack is defined.

---

##### `nestedStackParent`<sup>Optional</sup> <a name="nestedStackParent" id="cdk-constructs.ThronAcmCertificate.property.nestedStackParent"></a>

```typescript
public readonly nestedStackParent: Stack;
```

- *Type:* aws-cdk-lib.Stack

If this is a nested stack, returns it's parent stack.

---

##### `nestedStackResource`<sup>Optional</sup> <a name="nestedStackResource" id="cdk-constructs.ThronAcmCertificate.property.nestedStackResource"></a>

```typescript
public readonly nestedStackResource: CfnResource;
```

- *Type:* aws-cdk-lib.CfnResource

If this is a nested stack, this represents its `AWS::CloudFormation::Stack` resource.

`undefined` for top-level (non-nested) stacks.

---

##### `terminationProtection`<sup>Required</sup> <a name="terminationProtection" id="cdk-constructs.ThronAcmCertificate.property.terminationProtection"></a>

```typescript
public readonly terminationProtection: boolean;
```

- *Type:* boolean

Whether termination protection is enabled for this stack.

---

##### `certificate`<sup>Required</sup> <a name="certificate" id="cdk-constructs.ThronAcmCertificate.property.certificate"></a>

```typescript
public readonly certificate: Certificate;
```

- *Type:* aws-cdk-lib.aws_certificatemanager.Certificate

The issued certificate.

---

##### `domainName`<sup>Required</sup> <a name="domainName" id="cdk-constructs.ThronAcmCertificate.property.domainName"></a>

```typescript
public readonly domainName: string;
```

- *Type:* string

FQDN the certificate is issued for.

---

##### `subjectAlternativeNames`<sup>Optional</sup> <a name="subjectAlternativeNames" id="cdk-constructs.ThronAcmCertificate.property.subjectAlternativeNames"></a>

```typescript
public readonly subjectAlternativeNames: string[];
```

- *Type:* string[]

Alternative domain names on the certificate.

---


### ThronApiGatewayApi <a name="ThronApiGatewayApi" id="cdk-constructs.ThronApiGatewayApi"></a>

#### Initializers <a name="Initializers" id="cdk-constructs.ThronApiGatewayApi.Initializer"></a>

```typescript
import { ThronApiGatewayApi } from 'cdk-constructs'

new ThronApiGatewayApi(scope: Construct, id: string, props: ThronApiGatewayApiProps)
```

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.ThronApiGatewayApi.Initializer.parameter.scope">scope</a></code> | <code>constructs.Construct</code> | *No description.* |
| <code><a href="#cdk-constructs.ThronApiGatewayApi.Initializer.parameter.id">id</a></code> | <code>string</code> | *No description.* |
| <code><a href="#cdk-constructs.ThronApiGatewayApi.Initializer.parameter.props">props</a></code> | <code><a href="#cdk-constructs.ThronApiGatewayApiProps">ThronApiGatewayApiProps</a></code> | *No description.* |

---

##### `scope`<sup>Required</sup> <a name="scope" id="cdk-constructs.ThronApiGatewayApi.Initializer.parameter.scope"></a>

- *Type:* constructs.Construct

---

##### `id`<sup>Required</sup> <a name="id" id="cdk-constructs.ThronApiGatewayApi.Initializer.parameter.id"></a>

- *Type:* string

---

##### `props`<sup>Required</sup> <a name="props" id="cdk-constructs.ThronApiGatewayApi.Initializer.parameter.props"></a>

- *Type:* <a href="#cdk-constructs.ThronApiGatewayApiProps">ThronApiGatewayApiProps</a>

---

#### Methods <a name="Methods" id="Methods"></a>

| **Name** | **Description** |
| --- | --- |
| <code><a href="#cdk-constructs.ThronApiGatewayApi.toString">toString</a></code> | Returns a string representation of this construct. |
| <code><a href="#cdk-constructs.ThronApiGatewayApi.addAltDomain">addAltDomain</a></code> | *No description.* |
| <code><a href="#cdk-constructs.ThronApiGatewayApi.addLambdaEndpoint">addLambdaEndpoint</a></code> | *No description.* |
| <code><a href="#cdk-constructs.ThronApiGatewayApi.addServiceLambdaEndpoint">addServiceLambdaEndpoint</a></code> | *No description.* |

---

##### `toString` <a name="toString" id="cdk-constructs.ThronApiGatewayApi.toString"></a>

```typescript
public toString(): string
```

Returns a string representation of this construct.

##### `addAltDomain` <a name="addAltDomain" id="cdk-constructs.ThronApiGatewayApi.addAltDomain"></a>

```typescript
public addAltDomain(domainFirstPart: string): void
```

###### `domainFirstPart`<sup>Required</sup> <a name="domainFirstPart" id="cdk-constructs.ThronApiGatewayApi.addAltDomain.parameter.domainFirstPart"></a>

- *Type:* string

---

##### `addLambdaEndpoint` <a name="addLambdaEndpoint" id="cdk-constructs.ThronApiGatewayApi.addLambdaEndpoint"></a>

```typescript
public addLambdaEndpoint(lambdaFunction: IFunction, basePath: string, timeout: Duration): ThronEndpointApiGateway
```

###### `lambdaFunction`<sup>Required</sup> <a name="lambdaFunction" id="cdk-constructs.ThronApiGatewayApi.addLambdaEndpoint.parameter.lambdaFunction"></a>

- *Type:* aws-cdk-lib.aws_lambda.IFunction

---

###### `basePath`<sup>Required</sup> <a name="basePath" id="cdk-constructs.ThronApiGatewayApi.addLambdaEndpoint.parameter.basePath"></a>

- *Type:* string

---

###### `timeout`<sup>Required</sup> <a name="timeout" id="cdk-constructs.ThronApiGatewayApi.addLambdaEndpoint.parameter.timeout"></a>

- *Type:* aws-cdk-lib.Duration

---

##### `addServiceLambdaEndpoint` <a name="addServiceLambdaEndpoint" id="cdk-constructs.ThronApiGatewayApi.addServiceLambdaEndpoint"></a>

```typescript
public addServiceLambdaEndpoint(lambdaFunction: IFunction, timeout: Duration, __2: FullServiceProps): ThronEndpointApiGateway
```

###### `lambdaFunction`<sup>Required</sup> <a name="lambdaFunction" id="cdk-constructs.ThronApiGatewayApi.addServiceLambdaEndpoint.parameter.lambdaFunction"></a>

- *Type:* aws-cdk-lib.aws_lambda.IFunction

---

###### `timeout`<sup>Required</sup> <a name="timeout" id="cdk-constructs.ThronApiGatewayApi.addServiceLambdaEndpoint.parameter.timeout"></a>

- *Type:* aws-cdk-lib.Duration

---

###### `__2`<sup>Required</sup> <a name="__2" id="cdk-constructs.ThronApiGatewayApi.addServiceLambdaEndpoint.parameter.__2"></a>

- *Type:* <a href="#cdk-constructs.FullServiceProps">FullServiceProps</a>

---

#### Static Functions <a name="Static Functions" id="Static Functions"></a>

| **Name** | **Description** |
| --- | --- |
| <code><a href="#cdk-constructs.ThronApiGatewayApi.isConstruct">isConstruct</a></code> | Checks if `x` is a construct. |
| <code><a href="#cdk-constructs.ThronApiGatewayApi.buildServiceEndpoint">buildServiceEndpoint</a></code> | *No description.* |

---

##### `isConstruct` <a name="isConstruct" id="cdk-constructs.ThronApiGatewayApi.isConstruct"></a>

```typescript
import { ThronApiGatewayApi } from 'cdk-constructs'

ThronApiGatewayApi.isConstruct(x: any)
```

Checks if `x` is a construct.

Use this method instead of `instanceof` to properly detect `Construct`
instances, even when the construct library is symlinked.

Explanation: in JavaScript, multiple copies of the `constructs` library on
disk are seen as independent, completely different libraries. As a
consequence, the class `Construct` in each copy of the `constructs` library
is seen as a different class, and an instance of one class will not test as
`instanceof` the other class. `npm install` will not create installations
like this, but users may manually symlink construct libraries together or
use a monorepo tool: in those cases, multiple copies of the `constructs`
library can be accidentally installed, and `instanceof` will behave
unpredictably. It is safest to avoid using `instanceof`, and using
this type-testing method instead.

###### `x`<sup>Required</sup> <a name="x" id="cdk-constructs.ThronApiGatewayApi.isConstruct.parameter.x"></a>

- *Type:* any

Any object.

---

##### `buildServiceEndpoint` <a name="buildServiceEndpoint" id="cdk-constructs.ThronApiGatewayApi.buildServiceEndpoint"></a>

```typescript
import { ThronApiGatewayApi } from 'cdk-constructs'

ThronApiGatewayApi.buildServiceEndpoint(scope: Construct, serviceProps: FullServiceProps)
```

###### `scope`<sup>Required</sup> <a name="scope" id="cdk-constructs.ThronApiGatewayApi.buildServiceEndpoint.parameter.scope"></a>

- *Type:* constructs.Construct

---

###### `serviceProps`<sup>Required</sup> <a name="serviceProps" id="cdk-constructs.ThronApiGatewayApi.buildServiceEndpoint.parameter.serviceProps"></a>

- *Type:* <a href="#cdk-constructs.FullServiceProps">FullServiceProps</a>

---

#### Properties <a name="Properties" id="Properties"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.ThronApiGatewayApi.property.node">node</a></code> | <code>constructs.Node</code> | The tree node. |
| <code><a href="#cdk-constructs.ThronApiGatewayApi.property.apiGatewayApi">apiGatewayApi</a></code> | <code>aws-cdk-lib.aws_apigateway.RestApi</code> | *No description.* |
| <code><a href="#cdk-constructs.ThronApiGatewayApi.property.domainAliases">domainAliases</a></code> | <code><a href="#cdk-constructs.ThronApiGatewayDomainAlias">ThronApiGatewayDomainAlias</a>[]</code> | *No description.* |
| <code><a href="#cdk-constructs.ThronApiGatewayApi.property.mainDomain">mainDomain</a></code> | <code><a href="#cdk-constructs.ThronApiGatewayDomainAlias">ThronApiGatewayDomainAlias</a></code> | *No description.* |

---

##### `node`<sup>Required</sup> <a name="node" id="cdk-constructs.ThronApiGatewayApi.property.node"></a>

```typescript
public readonly node: Node;
```

- *Type:* constructs.Node

The tree node.

---

##### `apiGatewayApi`<sup>Required</sup> <a name="apiGatewayApi" id="cdk-constructs.ThronApiGatewayApi.property.apiGatewayApi"></a>

```typescript
public readonly apiGatewayApi: RestApi;
```

- *Type:* aws-cdk-lib.aws_apigateway.RestApi

---

##### `domainAliases`<sup>Required</sup> <a name="domainAliases" id="cdk-constructs.ThronApiGatewayApi.property.domainAliases"></a>

```typescript
public readonly domainAliases: ThronApiGatewayDomainAlias[];
```

- *Type:* <a href="#cdk-constructs.ThronApiGatewayDomainAlias">ThronApiGatewayDomainAlias</a>[]

---

##### `mainDomain`<sup>Required</sup> <a name="mainDomain" id="cdk-constructs.ThronApiGatewayApi.property.mainDomain"></a>

```typescript
public readonly mainDomain: ThronApiGatewayDomainAlias;
```

- *Type:* <a href="#cdk-constructs.ThronApiGatewayDomainAlias">ThronApiGatewayDomainAlias</a>

---


### ThronApiGatewayDomainAlias <a name="ThronApiGatewayDomainAlias" id="cdk-constructs.ThronApiGatewayDomainAlias"></a>

Defines an Alias domain to the main api-gateway.

*Example*

```typescript
const endpoint = new ThronApiGatewayDomainAlias(this, `cool-domain-alias`, {
    domainName: 'cool-domain.4me.cdndev.weebo.it',
    apiGatewayApi: sampleApi.restApiId,
    domainId: 'cool-domain'
  });
```


#### Initializers <a name="Initializers" id="cdk-constructs.ThronApiGatewayDomainAlias.Initializer"></a>

```typescript
import { ThronApiGatewayDomainAlias } from 'cdk-constructs'

new ThronApiGatewayDomainAlias(scope: Construct, id: string, props: ThronApiGatewayDomainAliasProps)
```

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.ThronApiGatewayDomainAlias.Initializer.parameter.scope">scope</a></code> | <code>constructs.Construct</code> | *No description.* |
| <code><a href="#cdk-constructs.ThronApiGatewayDomainAlias.Initializer.parameter.id">id</a></code> | <code>string</code> | *No description.* |
| <code><a href="#cdk-constructs.ThronApiGatewayDomainAlias.Initializer.parameter.props">props</a></code> | <code><a href="#cdk-constructs.ThronApiGatewayDomainAliasProps">ThronApiGatewayDomainAliasProps</a></code> | *No description.* |

---

##### `scope`<sup>Required</sup> <a name="scope" id="cdk-constructs.ThronApiGatewayDomainAlias.Initializer.parameter.scope"></a>

- *Type:* constructs.Construct

---

##### `id`<sup>Required</sup> <a name="id" id="cdk-constructs.ThronApiGatewayDomainAlias.Initializer.parameter.id"></a>

- *Type:* string

---

##### `props`<sup>Required</sup> <a name="props" id="cdk-constructs.ThronApiGatewayDomainAlias.Initializer.parameter.props"></a>

- *Type:* <a href="#cdk-constructs.ThronApiGatewayDomainAliasProps">ThronApiGatewayDomainAliasProps</a>

---

#### Methods <a name="Methods" id="Methods"></a>

| **Name** | **Description** |
| --- | --- |
| <code><a href="#cdk-constructs.ThronApiGatewayDomainAlias.toString">toString</a></code> | Returns a string representation of this construct. |

---

##### `toString` <a name="toString" id="cdk-constructs.ThronApiGatewayDomainAlias.toString"></a>

```typescript
public toString(): string
```

Returns a string representation of this construct.

#### Static Functions <a name="Static Functions" id="Static Functions"></a>

| **Name** | **Description** |
| --- | --- |
| <code><a href="#cdk-constructs.ThronApiGatewayDomainAlias.isConstruct">isConstruct</a></code> | Checks if `x` is a construct. |

---

##### `isConstruct` <a name="isConstruct" id="cdk-constructs.ThronApiGatewayDomainAlias.isConstruct"></a>

```typescript
import { ThronApiGatewayDomainAlias } from 'cdk-constructs'

ThronApiGatewayDomainAlias.isConstruct(x: any)
```

Checks if `x` is a construct.

Use this method instead of `instanceof` to properly detect `Construct`
instances, even when the construct library is symlinked.

Explanation: in JavaScript, multiple copies of the `constructs` library on
disk are seen as independent, completely different libraries. As a
consequence, the class `Construct` in each copy of the `constructs` library
is seen as a different class, and an instance of one class will not test as
`instanceof` the other class. `npm install` will not create installations
like this, but users may manually symlink construct libraries together or
use a monorepo tool: in those cases, multiple copies of the `constructs`
library can be accidentally installed, and `instanceof` will behave
unpredictably. It is safest to avoid using `instanceof`, and using
this type-testing method instead.

###### `x`<sup>Required</sup> <a name="x" id="cdk-constructs.ThronApiGatewayDomainAlias.isConstruct.parameter.x"></a>

- *Type:* any

Any object.

---

#### Properties <a name="Properties" id="Properties"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.ThronApiGatewayDomainAlias.property.node">node</a></code> | <code>constructs.Node</code> | The tree node. |
| <code><a href="#cdk-constructs.ThronApiGatewayDomainAlias.property.recordName">recordName</a></code> | <code>string</code> | *No description.* |

---

##### `node`<sup>Required</sup> <a name="node" id="cdk-constructs.ThronApiGatewayDomainAlias.property.node"></a>

```typescript
public readonly node: Node;
```

- *Type:* constructs.Node

The tree node.

---

##### `recordName`<sup>Required</sup> <a name="recordName" id="cdk-constructs.ThronApiGatewayDomainAlias.property.recordName"></a>

```typescript
public readonly recordName: string;
```

- *Type:* string

---


### ThronCachePolicy <a name="ThronCachePolicy" id="cdk-constructs.ThronCachePolicy"></a>

#### Methods <a name="Methods" id="Methods"></a>

| **Name** | **Description** |
| --- | --- |
| <code><a href="#cdk-constructs.ThronCachePolicy.toString">toString</a></code> | Returns a string representation of this construct. |
| <code><a href="#cdk-constructs.ThronCachePolicy.applyRemovalPolicy">applyRemovalPolicy</a></code> | Apply the given removal policy to this resource. |

---

##### `toString` <a name="toString" id="cdk-constructs.ThronCachePolicy.toString"></a>

```typescript
public toString(): string
```

Returns a string representation of this construct.

##### `applyRemovalPolicy` <a name="applyRemovalPolicy" id="cdk-constructs.ThronCachePolicy.applyRemovalPolicy"></a>

```typescript
public applyRemovalPolicy(policy: RemovalPolicy): void
```

Apply the given removal policy to this resource.

The Removal Policy controls what happens to this resource when it stops
being managed by CloudFormation, either because you've removed it from the
CDK application or because you've made a change that requires the resource
to be replaced.

The resource can be deleted (`RemovalPolicy.DESTROY`), or left in your AWS
account for data recovery and cleanup later (`RemovalPolicy.RETAIN`).

###### `policy`<sup>Required</sup> <a name="policy" id="cdk-constructs.ThronCachePolicy.applyRemovalPolicy.parameter.policy"></a>

- *Type:* aws-cdk-lib.RemovalPolicy

---

#### Static Functions <a name="Static Functions" id="Static Functions"></a>

| **Name** | **Description** |
| --- | --- |
| <code><a href="#cdk-constructs.ThronCachePolicy.isConstruct">isConstruct</a></code> | Checks if `x` is a construct. |
| <code><a href="#cdk-constructs.ThronCachePolicy.isOwnedResource">isOwnedResource</a></code> | Returns true if the construct was created by CDK, and false otherwise. |
| <code><a href="#cdk-constructs.ThronCachePolicy.isResource">isResource</a></code> | Check whether the given construct is a Resource. |
| <code><a href="#cdk-constructs.ThronCachePolicy.fromCachePolicyId">fromCachePolicyId</a></code> | Imports a Cache Policy from its id. |
| <code><a href="#cdk-constructs.ThronCachePolicy.cacheDisabled">cacheDisabled</a></code> | *No description.* |
| <code><a href="#cdk-constructs.ThronCachePolicy.default">default</a></code> | Generates a `ThronCachePolicy` with all the default values. |
| <code><a href="#cdk-constructs.ThronCachePolicy.defaultWithOverrides">defaultWithOverrides</a></code> | Generates a `ThronCachePolicy` with all the default values except for the ones passed on `props`. |

---

##### `isConstruct` <a name="isConstruct" id="cdk-constructs.ThronCachePolicy.isConstruct"></a>

```typescript
import { ThronCachePolicy } from 'cdk-constructs'

ThronCachePolicy.isConstruct(x: any)
```

Checks if `x` is a construct.

Use this method instead of `instanceof` to properly detect `Construct`
instances, even when the construct library is symlinked.

Explanation: in JavaScript, multiple copies of the `constructs` library on
disk are seen as independent, completely different libraries. As a
consequence, the class `Construct` in each copy of the `constructs` library
is seen as a different class, and an instance of one class will not test as
`instanceof` the other class. `npm install` will not create installations
like this, but users may manually symlink construct libraries together or
use a monorepo tool: in those cases, multiple copies of the `constructs`
library can be accidentally installed, and `instanceof` will behave
unpredictably. It is safest to avoid using `instanceof`, and using
this type-testing method instead.

###### `x`<sup>Required</sup> <a name="x" id="cdk-constructs.ThronCachePolicy.isConstruct.parameter.x"></a>

- *Type:* any

Any object.

---

##### `isOwnedResource` <a name="isOwnedResource" id="cdk-constructs.ThronCachePolicy.isOwnedResource"></a>

```typescript
import { ThronCachePolicy } from 'cdk-constructs'

ThronCachePolicy.isOwnedResource(construct: IConstruct)
```

Returns true if the construct was created by CDK, and false otherwise.

###### `construct`<sup>Required</sup> <a name="construct" id="cdk-constructs.ThronCachePolicy.isOwnedResource.parameter.construct"></a>

- *Type:* constructs.IConstruct

---

##### `isResource` <a name="isResource" id="cdk-constructs.ThronCachePolicy.isResource"></a>

```typescript
import { ThronCachePolicy } from 'cdk-constructs'

ThronCachePolicy.isResource(construct: IConstruct)
```

Check whether the given construct is a Resource.

###### `construct`<sup>Required</sup> <a name="construct" id="cdk-constructs.ThronCachePolicy.isResource.parameter.construct"></a>

- *Type:* constructs.IConstruct

---

##### `fromCachePolicyId` <a name="fromCachePolicyId" id="cdk-constructs.ThronCachePolicy.fromCachePolicyId"></a>

```typescript
import { ThronCachePolicy } from 'cdk-constructs'

ThronCachePolicy.fromCachePolicyId(scope: Construct, id: string, cachePolicyId: string)
```

Imports a Cache Policy from its id.

###### `scope`<sup>Required</sup> <a name="scope" id="cdk-constructs.ThronCachePolicy.fromCachePolicyId.parameter.scope"></a>

- *Type:* constructs.Construct

---

###### `id`<sup>Required</sup> <a name="id" id="cdk-constructs.ThronCachePolicy.fromCachePolicyId.parameter.id"></a>

- *Type:* string

---

###### `cachePolicyId`<sup>Required</sup> <a name="cachePolicyId" id="cdk-constructs.ThronCachePolicy.fromCachePolicyId.parameter.cachePolicyId"></a>

- *Type:* string

---

##### `cacheDisabled` <a name="cacheDisabled" id="cdk-constructs.ThronCachePolicy.cacheDisabled"></a>

```typescript
import { ThronCachePolicy } from 'cdk-constructs'

ThronCachePolicy.cacheDisabled(scope: Construct, id: string)
```

###### `scope`<sup>Required</sup> <a name="scope" id="cdk-constructs.ThronCachePolicy.cacheDisabled.parameter.scope"></a>

- *Type:* constructs.Construct

---

###### `id`<sup>Required</sup> <a name="id" id="cdk-constructs.ThronCachePolicy.cacheDisabled.parameter.id"></a>

- *Type:* string

---

##### `default` <a name="default" id="cdk-constructs.ThronCachePolicy.default"></a>

```typescript
import { ThronCachePolicy } from 'cdk-constructs'

ThronCachePolicy.default(scope: Construct, id: string)
```

Generates a `ThronCachePolicy` with all the default values.

###### `scope`<sup>Required</sup> <a name="scope" id="cdk-constructs.ThronCachePolicy.default.parameter.scope"></a>

- *Type:* constructs.Construct

---

###### `id`<sup>Required</sup> <a name="id" id="cdk-constructs.ThronCachePolicy.default.parameter.id"></a>

- *Type:* string

---

##### `defaultWithOverrides` <a name="defaultWithOverrides" id="cdk-constructs.ThronCachePolicy.defaultWithOverrides"></a>

```typescript
import { ThronCachePolicy } from 'cdk-constructs'

ThronCachePolicy.defaultWithOverrides(scope: Construct, id: string, props: ThronCachePolicyProps)
```

Generates a `ThronCachePolicy` with all the default values except for the ones passed on `props`.

###### `scope`<sup>Required</sup> <a name="scope" id="cdk-constructs.ThronCachePolicy.defaultWithOverrides.parameter.scope"></a>

- *Type:* constructs.Construct

---

###### `id`<sup>Required</sup> <a name="id" id="cdk-constructs.ThronCachePolicy.defaultWithOverrides.parameter.id"></a>

- *Type:* string

---

###### `props`<sup>Required</sup> <a name="props" id="cdk-constructs.ThronCachePolicy.defaultWithOverrides.parameter.props"></a>

- *Type:* <a href="#cdk-constructs.ThronCachePolicyProps">ThronCachePolicyProps</a>

---

#### Properties <a name="Properties" id="Properties"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.ThronCachePolicy.property.node">node</a></code> | <code>constructs.Node</code> | The tree node. |
| <code><a href="#cdk-constructs.ThronCachePolicy.property.env">env</a></code> | <code>aws-cdk-lib.ResourceEnvironment</code> | The environment this resource belongs to. |
| <code><a href="#cdk-constructs.ThronCachePolicy.property.stack">stack</a></code> | <code>aws-cdk-lib.Stack</code> | The stack in which this resource is defined. |
| <code><a href="#cdk-constructs.ThronCachePolicy.property.cachePolicyId">cachePolicyId</a></code> | <code>string</code> | The ID of the cache policy. |

---

##### `node`<sup>Required</sup> <a name="node" id="cdk-constructs.ThronCachePolicy.property.node"></a>

```typescript
public readonly node: Node;
```

- *Type:* constructs.Node

The tree node.

---

##### `env`<sup>Required</sup> <a name="env" id="cdk-constructs.ThronCachePolicy.property.env"></a>

```typescript
public readonly env: ResourceEnvironment;
```

- *Type:* aws-cdk-lib.ResourceEnvironment

The environment this resource belongs to.

For resources that are created and managed by the CDK
(generally, those created by creating new class instances like Role, Bucket, etc.),
this is always the same as the environment of the stack they belong to;
however, for imported resources
(those obtained from static methods like fromRoleArn, fromBucketName, etc.),
that might be different than the stack they were imported into.

---

##### `stack`<sup>Required</sup> <a name="stack" id="cdk-constructs.ThronCachePolicy.property.stack"></a>

```typescript
public readonly stack: Stack;
```

- *Type:* aws-cdk-lib.Stack

The stack in which this resource is defined.

---

##### `cachePolicyId`<sup>Required</sup> <a name="cachePolicyId" id="cdk-constructs.ThronCachePolicy.property.cachePolicyId"></a>

```typescript
public readonly cachePolicyId: string;
```

- *Type:* string

The ID of the cache policy.

---

#### Constants <a name="Constants" id="Constants"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.ThronCachePolicy.property.AMPLIFY">AMPLIFY</a></code> | <code>aws-cdk-lib.aws_cloudfront.ICachePolicy</code> | This policy is designed for use with an origin that is an AWS Amplify web app. |
| <code><a href="#cdk-constructs.ThronCachePolicy.property.CACHING_DISABLED">CACHING_DISABLED</a></code> | <code>aws-cdk-lib.aws_cloudfront.ICachePolicy</code> | Disables caching. |
| <code><a href="#cdk-constructs.ThronCachePolicy.property.CACHING_OPTIMIZED">CACHING_OPTIMIZED</a></code> | <code>aws-cdk-lib.aws_cloudfront.ICachePolicy</code> | Optimize cache efficiency by minimizing the values that CloudFront includes in the cache key. |
| <code><a href="#cdk-constructs.ThronCachePolicy.property.CACHING_OPTIMIZED_FOR_UNCOMPRESSED_OBJECTS">CACHING_OPTIMIZED_FOR_UNCOMPRESSED_OBJECTS</a></code> | <code>aws-cdk-lib.aws_cloudfront.ICachePolicy</code> | Optimize cache efficiency by minimizing the values that CloudFront includes in the cache key. |
| <code><a href="#cdk-constructs.ThronCachePolicy.property.ELEMENTAL_MEDIA_PACKAGE">ELEMENTAL_MEDIA_PACKAGE</a></code> | <code>aws-cdk-lib.aws_cloudfront.ICachePolicy</code> | Designed for use with an origin that is an AWS Elemental MediaPackage endpoint. |
| <code><a href="#cdk-constructs.ThronCachePolicy.property.USE_ORIGIN_CACHE_CONTROL_HEADERS">USE_ORIGIN_CACHE_CONTROL_HEADERS</a></code> | <code>aws-cdk-lib.aws_cloudfront.ICachePolicy</code> | Designed for use with an origin that returns Cache-Control HTTP response headers and does not serve different content based on values present in the query string. |
| <code><a href="#cdk-constructs.ThronCachePolicy.property.USE_ORIGIN_CACHE_CONTROL_HEADERS_QUERY_STRINGS">USE_ORIGIN_CACHE_CONTROL_HEADERS_QUERY_STRINGS</a></code> | <code>aws-cdk-lib.aws_cloudfront.ICachePolicy</code> | Designed for use with an origin that returns Cache-Control HTTP response headers and serves different content based on values present in the query string. |

---

##### `AMPLIFY`<sup>Required</sup> <a name="AMPLIFY" id="cdk-constructs.ThronCachePolicy.property.AMPLIFY"></a>

```typescript
public readonly AMPLIFY: ICachePolicy;
```

- *Type:* aws-cdk-lib.aws_cloudfront.ICachePolicy

This policy is designed for use with an origin that is an AWS Amplify web app.

---

##### `CACHING_DISABLED`<sup>Required</sup> <a name="CACHING_DISABLED" id="cdk-constructs.ThronCachePolicy.property.CACHING_DISABLED"></a>

```typescript
public readonly CACHING_DISABLED: ICachePolicy;
```

- *Type:* aws-cdk-lib.aws_cloudfront.ICachePolicy

Disables caching.

This policy is useful for dynamic content and for requests that are not cacheable.

---

##### `CACHING_OPTIMIZED`<sup>Required</sup> <a name="CACHING_OPTIMIZED" id="cdk-constructs.ThronCachePolicy.property.CACHING_OPTIMIZED"></a>

```typescript
public readonly CACHING_OPTIMIZED: ICachePolicy;
```

- *Type:* aws-cdk-lib.aws_cloudfront.ICachePolicy

Optimize cache efficiency by minimizing the values that CloudFront includes in the cache key.

Query strings and cookies are not included in the cache key, and only the normalized 'Accept-Encoding' header is included.

---

##### `CACHING_OPTIMIZED_FOR_UNCOMPRESSED_OBJECTS`<sup>Required</sup> <a name="CACHING_OPTIMIZED_FOR_UNCOMPRESSED_OBJECTS" id="cdk-constructs.ThronCachePolicy.property.CACHING_OPTIMIZED_FOR_UNCOMPRESSED_OBJECTS"></a>

```typescript
public readonly CACHING_OPTIMIZED_FOR_UNCOMPRESSED_OBJECTS: ICachePolicy;
```

- *Type:* aws-cdk-lib.aws_cloudfront.ICachePolicy

Optimize cache efficiency by minimizing the values that CloudFront includes in the cache key.

Query strings and cookies are not included in the cache key, and only the normalized 'Accept-Encoding' header is included.
Disables cache compression.

---

##### `ELEMENTAL_MEDIA_PACKAGE`<sup>Required</sup> <a name="ELEMENTAL_MEDIA_PACKAGE" id="cdk-constructs.ThronCachePolicy.property.ELEMENTAL_MEDIA_PACKAGE"></a>

```typescript
public readonly ELEMENTAL_MEDIA_PACKAGE: ICachePolicy;
```

- *Type:* aws-cdk-lib.aws_cloudfront.ICachePolicy

Designed for use with an origin that is an AWS Elemental MediaPackage endpoint.

---

##### `USE_ORIGIN_CACHE_CONTROL_HEADERS`<sup>Required</sup> <a name="USE_ORIGIN_CACHE_CONTROL_HEADERS" id="cdk-constructs.ThronCachePolicy.property.USE_ORIGIN_CACHE_CONTROL_HEADERS"></a>

```typescript
public readonly USE_ORIGIN_CACHE_CONTROL_HEADERS: ICachePolicy;
```

- *Type:* aws-cdk-lib.aws_cloudfront.ICachePolicy

Designed for use with an origin that returns Cache-Control HTTP response headers and does not serve different content based on values present in the query string.

---

##### `USE_ORIGIN_CACHE_CONTROL_HEADERS_QUERY_STRINGS`<sup>Required</sup> <a name="USE_ORIGIN_CACHE_CONTROL_HEADERS_QUERY_STRINGS" id="cdk-constructs.ThronCachePolicy.property.USE_ORIGIN_CACHE_CONTROL_HEADERS_QUERY_STRINGS"></a>

```typescript
public readonly USE_ORIGIN_CACHE_CONTROL_HEADERS_QUERY_STRINGS: ICachePolicy;
```

- *Type:* aws-cdk-lib.aws_cloudfront.ICachePolicy

Designed for use with an origin that returns Cache-Control HTTP response headers and serves different content based on values present in the query string.

---

### ThronCloudFrontDistribution <a name="ThronCloudFrontDistribution" id="cdk-constructs.ThronCloudFrontDistribution"></a>

#### Initializers <a name="Initializers" id="cdk-constructs.ThronCloudFrontDistribution.Initializer"></a>

```typescript
import { ThronCloudFrontDistribution } from 'cdk-constructs'

new ThronCloudFrontDistribution(scope: Stack, id: string, props: ThronCloudFrontDistributionProps)
```

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.ThronCloudFrontDistribution.Initializer.parameter.scope">scope</a></code> | <code>aws-cdk-lib.Stack</code> | *No description.* |
| <code><a href="#cdk-constructs.ThronCloudFrontDistribution.Initializer.parameter.id">id</a></code> | <code>string</code> | *No description.* |
| <code><a href="#cdk-constructs.ThronCloudFrontDistribution.Initializer.parameter.props">props</a></code> | <code><a href="#cdk-constructs.ThronCloudFrontDistributionProps">ThronCloudFrontDistributionProps</a></code> | *No description.* |

---

##### `scope`<sup>Required</sup> <a name="scope" id="cdk-constructs.ThronCloudFrontDistribution.Initializer.parameter.scope"></a>

- *Type:* aws-cdk-lib.Stack

---

##### `id`<sup>Required</sup> <a name="id" id="cdk-constructs.ThronCloudFrontDistribution.Initializer.parameter.id"></a>

- *Type:* string

---

##### `props`<sup>Required</sup> <a name="props" id="cdk-constructs.ThronCloudFrontDistribution.Initializer.parameter.props"></a>

- *Type:* <a href="#cdk-constructs.ThronCloudFrontDistributionProps">ThronCloudFrontDistributionProps</a>

---

#### Methods <a name="Methods" id="Methods"></a>

| **Name** | **Description** |
| --- | --- |
| <code><a href="#cdk-constructs.ThronCloudFrontDistribution.toString">toString</a></code> | Returns a string representation of this construct. |
| <code><a href="#cdk-constructs.ThronCloudFrontDistribution.isValidVersion">isValidVersion</a></code> | Validates `version` against frontend conventions. |

---

##### `toString` <a name="toString" id="cdk-constructs.ThronCloudFrontDistribution.toString"></a>

```typescript
public toString(): string
```

Returns a string representation of this construct.

##### `isValidVersion` <a name="isValidVersion" id="cdk-constructs.ThronCloudFrontDistribution.isValidVersion"></a>

```typescript
public isValidVersion(version?: string): boolean
```

Validates `version` against frontend conventions.

###### `version`<sup>Optional</sup> <a name="version" id="cdk-constructs.ThronCloudFrontDistribution.isValidVersion.parameter.version"></a>

- *Type:* string

---

#### Static Functions <a name="Static Functions" id="Static Functions"></a>

| **Name** | **Description** |
| --- | --- |
| <code><a href="#cdk-constructs.ThronCloudFrontDistribution.isConstruct">isConstruct</a></code> | Checks if `x` is a construct. |

---

##### `isConstruct` <a name="isConstruct" id="cdk-constructs.ThronCloudFrontDistribution.isConstruct"></a>

```typescript
import { ThronCloudFrontDistribution } from 'cdk-constructs'

ThronCloudFrontDistribution.isConstruct(x: any)
```

Checks if `x` is a construct.

Use this method instead of `instanceof` to properly detect `Construct`
instances, even when the construct library is symlinked.

Explanation: in JavaScript, multiple copies of the `constructs` library on
disk are seen as independent, completely different libraries. As a
consequence, the class `Construct` in each copy of the `constructs` library
is seen as a different class, and an instance of one class will not test as
`instanceof` the other class. `npm install` will not create installations
like this, but users may manually symlink construct libraries together or
use a monorepo tool: in those cases, multiple copies of the `constructs`
library can be accidentally installed, and `instanceof` will behave
unpredictably. It is safest to avoid using `instanceof`, and using
this type-testing method instead.

###### `x`<sup>Required</sup> <a name="x" id="cdk-constructs.ThronCloudFrontDistribution.isConstruct.parameter.x"></a>

- *Type:* any

Any object.

---

#### Properties <a name="Properties" id="Properties"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.ThronCloudFrontDistribution.property.node">node</a></code> | <code>constructs.Node</code> | The tree node. |
| <code><a href="#cdk-constructs.ThronCloudFrontDistribution.property.cachePolicy">cachePolicy</a></code> | <code>aws-cdk-lib.aws_cloudfront.CachePolicy</code> | Custom Cache Policy for the distribution. |
| <code><a href="#cdk-constructs.ThronCloudFrontDistribution.property.certificate">certificate</a></code> | <code>aws-cdk-lib.aws_certificatemanager.Certificate</code> | Certificate used for validating the domain name. |
| <code><a href="#cdk-constructs.ThronCloudFrontDistribution.property.defaultRootObject">defaultRootObject</a></code> | <code>string</code> | Object that you want CloudFront to request from your origin when a user requests the root URL for your distribution. |
| <code><a href="#cdk-constructs.ThronCloudFrontDistribution.property.defaultRootObjectCachePolicy">defaultRootObjectCachePolicy</a></code> | <code><a href="#cdk-constructs.ThronCachePolicy">ThronCachePolicy</a></code> | *No description.* |
| <code><a href="#cdk-constructs.ThronCloudFrontDistribution.property.defaultRootObjectResponseHeaderPolicy">defaultRootObjectResponseHeaderPolicy</a></code> | <code><a href="#cdk-constructs.ThronResponseHeaderPolicy">ThronResponseHeaderPolicy</a></code> | *No description.* |
| <code><a href="#cdk-constructs.ThronCloudFrontDistribution.property.deployBucket">deployBucket</a></code> | <code>aws-cdk-lib.aws_s3_deployment.BucketDeployment</code> | Populates an S3 bucket with the contents of .zip files from your local disk. |
| <code><a href="#cdk-constructs.ThronCloudFrontDistribution.property.description">description</a></code> | <code>string</code> | Description of the CloudFront Distribution. |
| <code><a href="#cdk-constructs.ThronCloudFrontDistribution.property.distribution">distribution</a></code> | <code>aws-cdk-lib.aws_cloudfront.Distribution</code> | CloudFront distribution with associated origins and caching behaviors. |
| <code><a href="#cdk-constructs.ThronCloudFrontDistribution.property.domainName">domainName</a></code> | <code>string</code> | Validated FQDN. |
| <code><a href="#cdk-constructs.ThronCloudFrontDistribution.property.oac">oac</a></code> | <code>aws-cdk-lib.aws_cloudfront.CfnOriginAccessControl</code> | Origin Access Control used to block public access to the S3 bucket so that users can access the content in the bucket only through CloudFront. |
| <code><a href="#cdk-constructs.ThronCloudFrontDistribution.property.responseHeaderPolicy">responseHeaderPolicy</a></code> | <code>aws-cdk-lib.aws_cloudfront.ResponseHeadersPolicy</code> | Custom Response Headers Policy. |
| <code><a href="#cdk-constructs.ThronCloudFrontDistribution.property.sourcePublicAsset">sourcePublicAsset</a></code> | <code>string</code> | Source path from which to deploy the contents of frontend. |
| <code><a href="#cdk-constructs.ThronCloudFrontDistribution.property.version">version</a></code> | <code>string</code> | Prefix key used for versioning. |
| <code><a href="#cdk-constructs.ThronCloudFrontDistribution.property.websiteBucket">websiteBucket</a></code> | <code>aws-cdk-lib.aws_s3.Bucket</code> | S3 Bucket where is stored the frontend static resources. |

---

##### `node`<sup>Required</sup> <a name="node" id="cdk-constructs.ThronCloudFrontDistribution.property.node"></a>

```typescript
public readonly node: Node;
```

- *Type:* constructs.Node

The tree node.

---

##### `cachePolicy`<sup>Required</sup> <a name="cachePolicy" id="cdk-constructs.ThronCloudFrontDistribution.property.cachePolicy"></a>

```typescript
public readonly cachePolicy: CachePolicy;
```

- *Type:* aws-cdk-lib.aws_cloudfront.CachePolicy

Custom Cache Policy for the distribution.

---

##### `certificate`<sup>Required</sup> <a name="certificate" id="cdk-constructs.ThronCloudFrontDistribution.property.certificate"></a>

```typescript
public readonly certificate: Certificate;
```

- *Type:* aws-cdk-lib.aws_certificatemanager.Certificate

Certificate used for validating the domain name.

---

##### `defaultRootObject`<sup>Required</sup> <a name="defaultRootObject" id="cdk-constructs.ThronCloudFrontDistribution.property.defaultRootObject"></a>

```typescript
public readonly defaultRootObject: string;
```

- *Type:* string

Object that you want CloudFront to request from your origin when a user requests the root URL for your distribution.

---

##### `defaultRootObjectCachePolicy`<sup>Required</sup> <a name="defaultRootObjectCachePolicy" id="cdk-constructs.ThronCloudFrontDistribution.property.defaultRootObjectCachePolicy"></a>

```typescript
public readonly defaultRootObjectCachePolicy: ThronCachePolicy;
```

- *Type:* <a href="#cdk-constructs.ThronCachePolicy">ThronCachePolicy</a>

---

##### `defaultRootObjectResponseHeaderPolicy`<sup>Required</sup> <a name="defaultRootObjectResponseHeaderPolicy" id="cdk-constructs.ThronCloudFrontDistribution.property.defaultRootObjectResponseHeaderPolicy"></a>

```typescript
public readonly defaultRootObjectResponseHeaderPolicy: ThronResponseHeaderPolicy;
```

- *Type:* <a href="#cdk-constructs.ThronResponseHeaderPolicy">ThronResponseHeaderPolicy</a>

---

##### `deployBucket`<sup>Required</sup> <a name="deployBucket" id="cdk-constructs.ThronCloudFrontDistribution.property.deployBucket"></a>

```typescript
public readonly deployBucket: BucketDeployment;
```

- *Type:* aws-cdk-lib.aws_s3_deployment.BucketDeployment

Populates an S3 bucket with the contents of .zip files from your local disk.

---

##### `description`<sup>Required</sup> <a name="description" id="cdk-constructs.ThronCloudFrontDistribution.property.description"></a>

```typescript
public readonly description: string;
```

- *Type:* string

Description of the CloudFront Distribution.

---

##### `distribution`<sup>Required</sup> <a name="distribution" id="cdk-constructs.ThronCloudFrontDistribution.property.distribution"></a>

```typescript
public readonly distribution: Distribution;
```

- *Type:* aws-cdk-lib.aws_cloudfront.Distribution

CloudFront distribution with associated origins and caching behaviors.

---

##### `domainName`<sup>Required</sup> <a name="domainName" id="cdk-constructs.ThronCloudFrontDistribution.property.domainName"></a>

```typescript
public readonly domainName: string;
```

- *Type:* string

Validated FQDN.

---

##### `oac`<sup>Required</sup> <a name="oac" id="cdk-constructs.ThronCloudFrontDistribution.property.oac"></a>

```typescript
public readonly oac: CfnOriginAccessControl;
```

- *Type:* aws-cdk-lib.aws_cloudfront.CfnOriginAccessControl

Origin Access Control used to block public access to the S3 bucket so that users can access the content in the bucket only through CloudFront.

---

##### `responseHeaderPolicy`<sup>Required</sup> <a name="responseHeaderPolicy" id="cdk-constructs.ThronCloudFrontDistribution.property.responseHeaderPolicy"></a>

```typescript
public readonly responseHeaderPolicy: ResponseHeadersPolicy;
```

- *Type:* aws-cdk-lib.aws_cloudfront.ResponseHeadersPolicy

Custom Response Headers Policy.

---

##### `sourcePublicAsset`<sup>Required</sup> <a name="sourcePublicAsset" id="cdk-constructs.ThronCloudFrontDistribution.property.sourcePublicAsset"></a>

```typescript
public readonly sourcePublicAsset: string;
```

- *Type:* string

Source path from which to deploy the contents of frontend.

---

##### `version`<sup>Required</sup> <a name="version" id="cdk-constructs.ThronCloudFrontDistribution.property.version"></a>

```typescript
public readonly version: string;
```

- *Type:* string

Prefix key used for versioning.

---

##### `websiteBucket`<sup>Required</sup> <a name="websiteBucket" id="cdk-constructs.ThronCloudFrontDistribution.property.websiteBucket"></a>

```typescript
public readonly websiteBucket: Bucket;
```

- *Type:* aws-cdk-lib.aws_s3.Bucket

S3 Bucket where is stored the frontend static resources.

---


### ThronDockerLambda <a name="ThronDockerLambda" id="cdk-constructs.ThronDockerLambda"></a>

#### Initializers <a name="Initializers" id="cdk-constructs.ThronDockerLambda.Initializer"></a>

```typescript
import { ThronDockerLambda } from 'cdk-constructs'

new ThronDockerLambda(scope: Stack, id: string, props: FunctionOptions)
```

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.ThronDockerLambda.Initializer.parameter.scope">scope</a></code> | <code>aws-cdk-lib.Stack</code> | *No description.* |
| <code><a href="#cdk-constructs.ThronDockerLambda.Initializer.parameter.id">id</a></code> | <code>string</code> | *No description.* |
| <code><a href="#cdk-constructs.ThronDockerLambda.Initializer.parameter.props">props</a></code> | <code><a href="#cdk-constructs.FunctionOptions">FunctionOptions</a></code> | *No description.* |

---

##### `scope`<sup>Required</sup> <a name="scope" id="cdk-constructs.ThronDockerLambda.Initializer.parameter.scope"></a>

- *Type:* aws-cdk-lib.Stack

---

##### `id`<sup>Required</sup> <a name="id" id="cdk-constructs.ThronDockerLambda.Initializer.parameter.id"></a>

- *Type:* string

---

##### `props`<sup>Required</sup> <a name="props" id="cdk-constructs.ThronDockerLambda.Initializer.parameter.props"></a>

- *Type:* <a href="#cdk-constructs.FunctionOptions">FunctionOptions</a>

---

#### Methods <a name="Methods" id="Methods"></a>

| **Name** | **Description** |
| --- | --- |
| <code><a href="#cdk-constructs.ThronDockerLambda.toString">toString</a></code> | Returns a string representation of this construct. |
| <code><a href="#cdk-constructs.ThronDockerLambda.applyRemovalPolicy">applyRemovalPolicy</a></code> | Apply the given removal policy to this resource. |
| <code><a href="#cdk-constructs.ThronDockerLambda.addEventSource">addEventSource</a></code> | Adds an event source to this function. |
| <code><a href="#cdk-constructs.ThronDockerLambda.addEventSourceMapping">addEventSourceMapping</a></code> | Adds an event source that maps to this AWS Lambda function. |
| <code><a href="#cdk-constructs.ThronDockerLambda.addFunctionUrl">addFunctionUrl</a></code> | Adds a url to this lambda function. |
| <code><a href="#cdk-constructs.ThronDockerLambda.addPermission">addPermission</a></code> | Adds a permission to the Lambda resource policy. |
| <code><a href="#cdk-constructs.ThronDockerLambda.addToRolePolicy">addToRolePolicy</a></code> | Adds a statement to the IAM role assumed by the instance. |
| <code><a href="#cdk-constructs.ThronDockerLambda.configureAsyncInvoke">configureAsyncInvoke</a></code> | Configures options for asynchronous invocation. |
| <code><a href="#cdk-constructs.ThronDockerLambda.considerWarningOnInvokeFunctionPermissions">considerWarningOnInvokeFunctionPermissions</a></code> | A warning will be added to functions under the following conditions: - permissions that include `lambda:InvokeFunction` are added to the unqualified function. |
| <code><a href="#cdk-constructs.ThronDockerLambda.grantInvoke">grantInvoke</a></code> | Grant the given identity permissions to invoke this Lambda. |
| <code><a href="#cdk-constructs.ThronDockerLambda.grantInvokeCompositePrincipal">grantInvokeCompositePrincipal</a></code> | Grant multiple principals the ability to invoke this Lambda via CompositePrincipal. |
| <code><a href="#cdk-constructs.ThronDockerLambda.grantInvokeLatestVersion">grantInvokeLatestVersion</a></code> | Grant the given identity permissions to invoke the $LATEST version or unqualified version of this Lambda. |
| <code><a href="#cdk-constructs.ThronDockerLambda.grantInvokeUrl">grantInvokeUrl</a></code> | Grant the given identity permissions to invoke this Lambda Function URL. |
| <code><a href="#cdk-constructs.ThronDockerLambda.grantInvokeVersion">grantInvokeVersion</a></code> | Grant the given identity permissions to invoke the given version of this Lambda. |
| <code><a href="#cdk-constructs.ThronDockerLambda.metric">metric</a></code> | Return the given named metric for this Function. |
| <code><a href="#cdk-constructs.ThronDockerLambda.metricDuration">metricDuration</a></code> | How long execution of this Lambda takes. |
| <code><a href="#cdk-constructs.ThronDockerLambda.metricErrors">metricErrors</a></code> | How many invocations of this Lambda fail. |
| <code><a href="#cdk-constructs.ThronDockerLambda.metricInvocations">metricInvocations</a></code> | How often this Lambda is invoked. |
| <code><a href="#cdk-constructs.ThronDockerLambda.metricThrottles">metricThrottles</a></code> | How often this Lambda is throttled. |
| <code><a href="#cdk-constructs.ThronDockerLambda.addAlias">addAlias</a></code> | Defines an alias for this function. |
| <code><a href="#cdk-constructs.ThronDockerLambda.addEnvironment">addEnvironment</a></code> | Adds an environment variable to this Lambda function. |
| <code><a href="#cdk-constructs.ThronDockerLambda.addLayers">addLayers</a></code> | Adds one or more Lambda Layers to this Lambda function. |
| <code><a href="#cdk-constructs.ThronDockerLambda.invalidateVersionBasedOn">invalidateVersionBasedOn</a></code> | Mix additional information into the hash of the Version object. |
| <code><a href="#cdk-constructs.ThronDockerLambda.addEndpointAlb">addEndpointAlb</a></code> | Add an endpoint the lambda function. |
| <code><a href="#cdk-constructs.ThronDockerLambda.addLegacyEndpointAlb">addLegacyEndpointAlb</a></code> | Add a legacy endpoint to the lambda function. |

---

##### `toString` <a name="toString" id="cdk-constructs.ThronDockerLambda.toString"></a>

```typescript
public toString(): string
```

Returns a string representation of this construct.

##### `applyRemovalPolicy` <a name="applyRemovalPolicy" id="cdk-constructs.ThronDockerLambda.applyRemovalPolicy"></a>

```typescript
public applyRemovalPolicy(policy: RemovalPolicy): void
```

Apply the given removal policy to this resource.

The Removal Policy controls what happens to this resource when it stops
being managed by CloudFormation, either because you've removed it from the
CDK application or because you've made a change that requires the resource
to be replaced.

The resource can be deleted (`RemovalPolicy.DESTROY`), or left in your AWS
account for data recovery and cleanup later (`RemovalPolicy.RETAIN`).

###### `policy`<sup>Required</sup> <a name="policy" id="cdk-constructs.ThronDockerLambda.applyRemovalPolicy.parameter.policy"></a>

- *Type:* aws-cdk-lib.RemovalPolicy

---

##### `addEventSource` <a name="addEventSource" id="cdk-constructs.ThronDockerLambda.addEventSource"></a>

```typescript
public addEventSource(source: IEventSource): void
```

Adds an event source to this function.

Event sources are implemented in the aws-cdk-lib/aws-lambda-event-sources module.

The following example adds an SQS Queue as an event source:
```
import { SqsEventSource } from 'aws-cdk-lib/aws-lambda-event-sources';
myFunction.addEventSource(new SqsEventSource(myQueue));
```

###### `source`<sup>Required</sup> <a name="source" id="cdk-constructs.ThronDockerLambda.addEventSource.parameter.source"></a>

- *Type:* aws-cdk-lib.aws_lambda.IEventSource

---

##### `addEventSourceMapping` <a name="addEventSourceMapping" id="cdk-constructs.ThronDockerLambda.addEventSourceMapping"></a>

```typescript
public addEventSourceMapping(id: string, options: EventSourceMappingOptions): EventSourceMapping
```

Adds an event source that maps to this AWS Lambda function.

###### `id`<sup>Required</sup> <a name="id" id="cdk-constructs.ThronDockerLambda.addEventSourceMapping.parameter.id"></a>

- *Type:* string

---

###### `options`<sup>Required</sup> <a name="options" id="cdk-constructs.ThronDockerLambda.addEventSourceMapping.parameter.options"></a>

- *Type:* aws-cdk-lib.aws_lambda.EventSourceMappingOptions

---

##### `addFunctionUrl` <a name="addFunctionUrl" id="cdk-constructs.ThronDockerLambda.addFunctionUrl"></a>

```typescript
public addFunctionUrl(options?: FunctionUrlOptions): FunctionUrl
```

Adds a url to this lambda function.

###### `options`<sup>Optional</sup> <a name="options" id="cdk-constructs.ThronDockerLambda.addFunctionUrl.parameter.options"></a>

- *Type:* aws-cdk-lib.aws_lambda.FunctionUrlOptions

---

##### `addPermission` <a name="addPermission" id="cdk-constructs.ThronDockerLambda.addPermission"></a>

```typescript
public addPermission(id: string, permission: Permission): void
```

Adds a permission to the Lambda resource policy.

> [Permission for details.](Permission for details.)

###### `id`<sup>Required</sup> <a name="id" id="cdk-constructs.ThronDockerLambda.addPermission.parameter.id"></a>

- *Type:* string

The id for the permission construct.

---

###### `permission`<sup>Required</sup> <a name="permission" id="cdk-constructs.ThronDockerLambda.addPermission.parameter.permission"></a>

- *Type:* aws-cdk-lib.aws_lambda.Permission

The permission to grant to this Lambda function.

---

##### `addToRolePolicy` <a name="addToRolePolicy" id="cdk-constructs.ThronDockerLambda.addToRolePolicy"></a>

```typescript
public addToRolePolicy(statement: PolicyStatement): void
```

Adds a statement to the IAM role assumed by the instance.

###### `statement`<sup>Required</sup> <a name="statement" id="cdk-constructs.ThronDockerLambda.addToRolePolicy.parameter.statement"></a>

- *Type:* aws-cdk-lib.aws_iam.PolicyStatement

---

##### `configureAsyncInvoke` <a name="configureAsyncInvoke" id="cdk-constructs.ThronDockerLambda.configureAsyncInvoke"></a>

```typescript
public configureAsyncInvoke(options: EventInvokeConfigOptions): void
```

Configures options for asynchronous invocation.

###### `options`<sup>Required</sup> <a name="options" id="cdk-constructs.ThronDockerLambda.configureAsyncInvoke.parameter.options"></a>

- *Type:* aws-cdk-lib.aws_lambda.EventInvokeConfigOptions

---

##### `considerWarningOnInvokeFunctionPermissions` <a name="considerWarningOnInvokeFunctionPermissions" id="cdk-constructs.ThronDockerLambda.considerWarningOnInvokeFunctionPermissions"></a>

```typescript
public considerWarningOnInvokeFunctionPermissions(scope: Construct, action: string): void
```

A warning will be added to functions under the following conditions: - permissions that include `lambda:InvokeFunction` are added to the unqualified function.

function.currentVersion is invoked before or after the permission is created.

This applies only to permissions on Lambda functions, not versions or aliases.
This function is overridden as a noOp for QualifiedFunctionBase.

###### `scope`<sup>Required</sup> <a name="scope" id="cdk-constructs.ThronDockerLambda.considerWarningOnInvokeFunctionPermissions.parameter.scope"></a>

- *Type:* constructs.Construct

---

###### `action`<sup>Required</sup> <a name="action" id="cdk-constructs.ThronDockerLambda.considerWarningOnInvokeFunctionPermissions.parameter.action"></a>

- *Type:* string

---

##### `grantInvoke` <a name="grantInvoke" id="cdk-constructs.ThronDockerLambda.grantInvoke"></a>

```typescript
public grantInvoke(grantee: IGrantable): Grant
```

Grant the given identity permissions to invoke this Lambda.

###### `grantee`<sup>Required</sup> <a name="grantee" id="cdk-constructs.ThronDockerLambda.grantInvoke.parameter.grantee"></a>

- *Type:* aws-cdk-lib.aws_iam.IGrantable

---

##### `grantInvokeCompositePrincipal` <a name="grantInvokeCompositePrincipal" id="cdk-constructs.ThronDockerLambda.grantInvokeCompositePrincipal"></a>

```typescript
public grantInvokeCompositePrincipal(compositePrincipal: CompositePrincipal): Grant[]
```

Grant multiple principals the ability to invoke this Lambda via CompositePrincipal.

###### `compositePrincipal`<sup>Required</sup> <a name="compositePrincipal" id="cdk-constructs.ThronDockerLambda.grantInvokeCompositePrincipal.parameter.compositePrincipal"></a>

- *Type:* aws-cdk-lib.aws_iam.CompositePrincipal

---

##### `grantInvokeLatestVersion` <a name="grantInvokeLatestVersion" id="cdk-constructs.ThronDockerLambda.grantInvokeLatestVersion"></a>

```typescript
public grantInvokeLatestVersion(grantee: IGrantable): Grant
```

Grant the given identity permissions to invoke the $LATEST version or unqualified version of this Lambda.

###### `grantee`<sup>Required</sup> <a name="grantee" id="cdk-constructs.ThronDockerLambda.grantInvokeLatestVersion.parameter.grantee"></a>

- *Type:* aws-cdk-lib.aws_iam.IGrantable

---

##### `grantInvokeUrl` <a name="grantInvokeUrl" id="cdk-constructs.ThronDockerLambda.grantInvokeUrl"></a>

```typescript
public grantInvokeUrl(grantee: IGrantable): Grant
```

Grant the given identity permissions to invoke this Lambda Function URL.

###### `grantee`<sup>Required</sup> <a name="grantee" id="cdk-constructs.ThronDockerLambda.grantInvokeUrl.parameter.grantee"></a>

- *Type:* aws-cdk-lib.aws_iam.IGrantable

---

##### `grantInvokeVersion` <a name="grantInvokeVersion" id="cdk-constructs.ThronDockerLambda.grantInvokeVersion"></a>

```typescript
public grantInvokeVersion(grantee: IGrantable, version: IVersion): Grant
```

Grant the given identity permissions to invoke the given version of this Lambda.

###### `grantee`<sup>Required</sup> <a name="grantee" id="cdk-constructs.ThronDockerLambda.grantInvokeVersion.parameter.grantee"></a>

- *Type:* aws-cdk-lib.aws_iam.IGrantable

---

###### `version`<sup>Required</sup> <a name="version" id="cdk-constructs.ThronDockerLambda.grantInvokeVersion.parameter.version"></a>

- *Type:* aws-cdk-lib.aws_lambda.IVersion

---

##### `metric` <a name="metric" id="cdk-constructs.ThronDockerLambda.metric"></a>

```typescript
public metric(metricName: string, props?: MetricOptions): Metric
```

Return the given named metric for this Function.

###### `metricName`<sup>Required</sup> <a name="metricName" id="cdk-constructs.ThronDockerLambda.metric.parameter.metricName"></a>

- *Type:* string

---

###### `props`<sup>Optional</sup> <a name="props" id="cdk-constructs.ThronDockerLambda.metric.parameter.props"></a>

- *Type:* aws-cdk-lib.aws_cloudwatch.MetricOptions

---

##### `metricDuration` <a name="metricDuration" id="cdk-constructs.ThronDockerLambda.metricDuration"></a>

```typescript
public metricDuration(props?: MetricOptions): Metric
```

How long execution of this Lambda takes.

Average over 5 minutes

###### `props`<sup>Optional</sup> <a name="props" id="cdk-constructs.ThronDockerLambda.metricDuration.parameter.props"></a>

- *Type:* aws-cdk-lib.aws_cloudwatch.MetricOptions

---

##### `metricErrors` <a name="metricErrors" id="cdk-constructs.ThronDockerLambda.metricErrors"></a>

```typescript
public metricErrors(props?: MetricOptions): Metric
```

How many invocations of this Lambda fail.

Sum over 5 minutes

###### `props`<sup>Optional</sup> <a name="props" id="cdk-constructs.ThronDockerLambda.metricErrors.parameter.props"></a>

- *Type:* aws-cdk-lib.aws_cloudwatch.MetricOptions

---

##### `metricInvocations` <a name="metricInvocations" id="cdk-constructs.ThronDockerLambda.metricInvocations"></a>

```typescript
public metricInvocations(props?: MetricOptions): Metric
```

How often this Lambda is invoked.

Sum over 5 minutes

###### `props`<sup>Optional</sup> <a name="props" id="cdk-constructs.ThronDockerLambda.metricInvocations.parameter.props"></a>

- *Type:* aws-cdk-lib.aws_cloudwatch.MetricOptions

---

##### `metricThrottles` <a name="metricThrottles" id="cdk-constructs.ThronDockerLambda.metricThrottles"></a>

```typescript
public metricThrottles(props?: MetricOptions): Metric
```

How often this Lambda is throttled.

Sum over 5 minutes

###### `props`<sup>Optional</sup> <a name="props" id="cdk-constructs.ThronDockerLambda.metricThrottles.parameter.props"></a>

- *Type:* aws-cdk-lib.aws_cloudwatch.MetricOptions

---

##### `addAlias` <a name="addAlias" id="cdk-constructs.ThronDockerLambda.addAlias"></a>

```typescript
public addAlias(aliasName: string, options?: AliasOptions): Alias
```

Defines an alias for this function.

The alias will automatically be updated to point to the latest version of
the function as it is being updated during a deployment.

```ts
declare const fn: lambda.Function;

fn.addAlias('Live');

// Is equivalent to

new lambda.Alias(this, 'AliasLive', {
  aliasName: 'Live',
  version: fn.currentVersion,
});
```

###### `aliasName`<sup>Required</sup> <a name="aliasName" id="cdk-constructs.ThronDockerLambda.addAlias.parameter.aliasName"></a>

- *Type:* string

The name of the alias.

---

###### `options`<sup>Optional</sup> <a name="options" id="cdk-constructs.ThronDockerLambda.addAlias.parameter.options"></a>

- *Type:* aws-cdk-lib.aws_lambda.AliasOptions

Alias options.

---

##### `addEnvironment` <a name="addEnvironment" id="cdk-constructs.ThronDockerLambda.addEnvironment"></a>

```typescript
public addEnvironment(key: string, value: string, options?: EnvironmentOptions): Function
```

Adds an environment variable to this Lambda function.

If this is a ref to a Lambda function, this operation results in a no-op.

###### `key`<sup>Required</sup> <a name="key" id="cdk-constructs.ThronDockerLambda.addEnvironment.parameter.key"></a>

- *Type:* string

The environment variable key.

---

###### `value`<sup>Required</sup> <a name="value" id="cdk-constructs.ThronDockerLambda.addEnvironment.parameter.value"></a>

- *Type:* string

The environment variable's value.

---

###### `options`<sup>Optional</sup> <a name="options" id="cdk-constructs.ThronDockerLambda.addEnvironment.parameter.options"></a>

- *Type:* aws-cdk-lib.aws_lambda.EnvironmentOptions

Environment variable options.

---

##### `addLayers` <a name="addLayers" id="cdk-constructs.ThronDockerLambda.addLayers"></a>

```typescript
public addLayers(layers: ILayerVersion): void
```

Adds one or more Lambda Layers to this Lambda function.

###### `layers`<sup>Required</sup> <a name="layers" id="cdk-constructs.ThronDockerLambda.addLayers.parameter.layers"></a>

- *Type:* aws-cdk-lib.aws_lambda.ILayerVersion

the layers to be added.

---

##### `invalidateVersionBasedOn` <a name="invalidateVersionBasedOn" id="cdk-constructs.ThronDockerLambda.invalidateVersionBasedOn"></a>

```typescript
public invalidateVersionBasedOn(x: string): void
```

Mix additional information into the hash of the Version object.

The Lambda Function construct does its best to automatically create a new
Version when anything about the Function changes (its code, its layers,
any of the other properties).

However, you can sometimes source information from places that the CDK cannot
look into, like the deploy-time values of SSM parameters. In those cases,
the CDK would not force the creation of a new Version object when it actually
should.

This method can be used to invalidate the current Version object. Pass in
any string into this method, and make sure the string changes when you know
a new Version needs to be created.

This method may be called more than once.

###### `x`<sup>Required</sup> <a name="x" id="cdk-constructs.ThronDockerLambda.invalidateVersionBasedOn.parameter.x"></a>

- *Type:* string

---

##### `addEndpointAlb` <a name="addEndpointAlb" id="cdk-constructs.ThronDockerLambda.addEndpointAlb"></a>

```typescript
public addEndpointAlb(name: string, endpointProps: ThronEndpointAlbProps): EndpointAlb
```

Add an endpoint the lambda function.

###### `name`<sup>Required</sup> <a name="name" id="cdk-constructs.ThronDockerLambda.addEndpointAlb.parameter.name"></a>

- *Type:* string

---

###### `endpointProps`<sup>Required</sup> <a name="endpointProps" id="cdk-constructs.ThronDockerLambda.addEndpointAlb.parameter.endpointProps"></a>

- *Type:* <a href="#cdk-constructs.ThronEndpointAlbProps">ThronEndpointAlbProps</a>

---

##### `addLegacyEndpointAlb` <a name="addLegacyEndpointAlb" id="cdk-constructs.ThronDockerLambda.addLegacyEndpointAlb"></a>

```typescript
public addLegacyEndpointAlb(name: string, endpointProps: LegacyEndpointAlbProps): EndpointAlb
```

Add a legacy endpoint to the lambda function.

###### `name`<sup>Required</sup> <a name="name" id="cdk-constructs.ThronDockerLambda.addLegacyEndpointAlb.parameter.name"></a>

- *Type:* string

---

###### `endpointProps`<sup>Required</sup> <a name="endpointProps" id="cdk-constructs.ThronDockerLambda.addLegacyEndpointAlb.parameter.endpointProps"></a>

- *Type:* <a href="#cdk-constructs.LegacyEndpointAlbProps">LegacyEndpointAlbProps</a>

---

#### Static Functions <a name="Static Functions" id="Static Functions"></a>

| **Name** | **Description** |
| --- | --- |
| <code><a href="#cdk-constructs.ThronDockerLambda.isConstruct">isConstruct</a></code> | Checks if `x` is a construct. |
| <code><a href="#cdk-constructs.ThronDockerLambda.isOwnedResource">isOwnedResource</a></code> | Returns true if the construct was created by CDK, and false otherwise. |
| <code><a href="#cdk-constructs.ThronDockerLambda.isResource">isResource</a></code> | Check whether the given construct is a Resource. |
| <code><a href="#cdk-constructs.ThronDockerLambda.classifyVersionProperty">classifyVersionProperty</a></code> | Record whether specific properties in the `AWS::Lambda::Function` resource should also be associated to the Version resource. |
| <code><a href="#cdk-constructs.ThronDockerLambda.fromFunctionArn">fromFunctionArn</a></code> | Import a lambda function into the CDK using its ARN. |
| <code><a href="#cdk-constructs.ThronDockerLambda.fromFunctionAttributes">fromFunctionAttributes</a></code> | Creates a Lambda function object which represents a function not defined within this stack. |
| <code><a href="#cdk-constructs.ThronDockerLambda.fromFunctionName">fromFunctionName</a></code> | Import a lambda function into the CDK using its name. |
| <code><a href="#cdk-constructs.ThronDockerLambda.metricAll">metricAll</a></code> | Return the given named metric for this Lambda. |
| <code><a href="#cdk-constructs.ThronDockerLambda.metricAllConcurrentExecutions">metricAllConcurrentExecutions</a></code> | Metric for the number of concurrent executions across all Lambdas. |
| <code><a href="#cdk-constructs.ThronDockerLambda.metricAllDuration">metricAllDuration</a></code> | Metric for the Duration executing all Lambdas. |
| <code><a href="#cdk-constructs.ThronDockerLambda.metricAllErrors">metricAllErrors</a></code> | Metric for the number of Errors executing all Lambdas. |
| <code><a href="#cdk-constructs.ThronDockerLambda.metricAllInvocations">metricAllInvocations</a></code> | Metric for the number of invocations of all Lambdas. |
| <code><a href="#cdk-constructs.ThronDockerLambda.metricAllThrottles">metricAllThrottles</a></code> | Metric for the number of throttled invocations of all Lambdas. |
| <code><a href="#cdk-constructs.ThronDockerLambda.metricAllUnreservedConcurrentExecutions">metricAllUnreservedConcurrentExecutions</a></code> | Metric for the number of unreserved concurrent executions across all Lambdas. |

---

##### `isConstruct` <a name="isConstruct" id="cdk-constructs.ThronDockerLambda.isConstruct"></a>

```typescript
import { ThronDockerLambda } from 'cdk-constructs'

ThronDockerLambda.isConstruct(x: any)
```

Checks if `x` is a construct.

Use this method instead of `instanceof` to properly detect `Construct`
instances, even when the construct library is symlinked.

Explanation: in JavaScript, multiple copies of the `constructs` library on
disk are seen as independent, completely different libraries. As a
consequence, the class `Construct` in each copy of the `constructs` library
is seen as a different class, and an instance of one class will not test as
`instanceof` the other class. `npm install` will not create installations
like this, but users may manually symlink construct libraries together or
use a monorepo tool: in those cases, multiple copies of the `constructs`
library can be accidentally installed, and `instanceof` will behave
unpredictably. It is safest to avoid using `instanceof`, and using
this type-testing method instead.

###### `x`<sup>Required</sup> <a name="x" id="cdk-constructs.ThronDockerLambda.isConstruct.parameter.x"></a>

- *Type:* any

Any object.

---

##### `isOwnedResource` <a name="isOwnedResource" id="cdk-constructs.ThronDockerLambda.isOwnedResource"></a>

```typescript
import { ThronDockerLambda } from 'cdk-constructs'

ThronDockerLambda.isOwnedResource(construct: IConstruct)
```

Returns true if the construct was created by CDK, and false otherwise.

###### `construct`<sup>Required</sup> <a name="construct" id="cdk-constructs.ThronDockerLambda.isOwnedResource.parameter.construct"></a>

- *Type:* constructs.IConstruct

---

##### `isResource` <a name="isResource" id="cdk-constructs.ThronDockerLambda.isResource"></a>

```typescript
import { ThronDockerLambda } from 'cdk-constructs'

ThronDockerLambda.isResource(construct: IConstruct)
```

Check whether the given construct is a Resource.

###### `construct`<sup>Required</sup> <a name="construct" id="cdk-constructs.ThronDockerLambda.isResource.parameter.construct"></a>

- *Type:* constructs.IConstruct

---

##### `classifyVersionProperty` <a name="classifyVersionProperty" id="cdk-constructs.ThronDockerLambda.classifyVersionProperty"></a>

```typescript
import { ThronDockerLambda } from 'cdk-constructs'

ThronDockerLambda.classifyVersionProperty(propertyName: string, locked: boolean)
```

Record whether specific properties in the `AWS::Lambda::Function` resource should also be associated to the Version resource.

See 'currentVersion' section in the module README for more details.

###### `propertyName`<sup>Required</sup> <a name="propertyName" id="cdk-constructs.ThronDockerLambda.classifyVersionProperty.parameter.propertyName"></a>

- *Type:* string

The property to classify.

---

###### `locked`<sup>Required</sup> <a name="locked" id="cdk-constructs.ThronDockerLambda.classifyVersionProperty.parameter.locked"></a>

- *Type:* boolean

whether the property should be associated to the version or not.

---

##### `fromFunctionArn` <a name="fromFunctionArn" id="cdk-constructs.ThronDockerLambda.fromFunctionArn"></a>

```typescript
import { ThronDockerLambda } from 'cdk-constructs'

ThronDockerLambda.fromFunctionArn(scope: Construct, id: string, functionArn: string)
```

Import a lambda function into the CDK using its ARN.

For `Function.addPermissions()` to work on this imported lambda, make sure that is
in the same account and region as the stack you are importing it into.

###### `scope`<sup>Required</sup> <a name="scope" id="cdk-constructs.ThronDockerLambda.fromFunctionArn.parameter.scope"></a>

- *Type:* constructs.Construct

---

###### `id`<sup>Required</sup> <a name="id" id="cdk-constructs.ThronDockerLambda.fromFunctionArn.parameter.id"></a>

- *Type:* string

---

###### `functionArn`<sup>Required</sup> <a name="functionArn" id="cdk-constructs.ThronDockerLambda.fromFunctionArn.parameter.functionArn"></a>

- *Type:* string

---

##### `fromFunctionAttributes` <a name="fromFunctionAttributes" id="cdk-constructs.ThronDockerLambda.fromFunctionAttributes"></a>

```typescript
import { ThronDockerLambda } from 'cdk-constructs'

ThronDockerLambda.fromFunctionAttributes(scope: Construct, id: string, attrs: FunctionAttributes)
```

Creates a Lambda function object which represents a function not defined within this stack.

For `Function.addPermissions()` to work on this imported lambda, set the sameEnvironment property to true
if this imported lambda is in the same account and region as the stack you are importing it into.

###### `scope`<sup>Required</sup> <a name="scope" id="cdk-constructs.ThronDockerLambda.fromFunctionAttributes.parameter.scope"></a>

- *Type:* constructs.Construct

The parent construct.

---

###### `id`<sup>Required</sup> <a name="id" id="cdk-constructs.ThronDockerLambda.fromFunctionAttributes.parameter.id"></a>

- *Type:* string

The name of the lambda construct.

---

###### `attrs`<sup>Required</sup> <a name="attrs" id="cdk-constructs.ThronDockerLambda.fromFunctionAttributes.parameter.attrs"></a>

- *Type:* aws-cdk-lib.aws_lambda.FunctionAttributes

the attributes of the function to import.

---

##### `fromFunctionName` <a name="fromFunctionName" id="cdk-constructs.ThronDockerLambda.fromFunctionName"></a>

```typescript
import { ThronDockerLambda } from 'cdk-constructs'

ThronDockerLambda.fromFunctionName(scope: Construct, id: string, functionName: string)
```

Import a lambda function into the CDK using its name.

###### `scope`<sup>Required</sup> <a name="scope" id="cdk-constructs.ThronDockerLambda.fromFunctionName.parameter.scope"></a>

- *Type:* constructs.Construct

---

###### `id`<sup>Required</sup> <a name="id" id="cdk-constructs.ThronDockerLambda.fromFunctionName.parameter.id"></a>

- *Type:* string

---

###### `functionName`<sup>Required</sup> <a name="functionName" id="cdk-constructs.ThronDockerLambda.fromFunctionName.parameter.functionName"></a>

- *Type:* string

---

##### `metricAll` <a name="metricAll" id="cdk-constructs.ThronDockerLambda.metricAll"></a>

```typescript
import { ThronDockerLambda } from 'cdk-constructs'

ThronDockerLambda.metricAll(metricName: string, props?: MetricOptions)
```

Return the given named metric for this Lambda.

###### `metricName`<sup>Required</sup> <a name="metricName" id="cdk-constructs.ThronDockerLambda.metricAll.parameter.metricName"></a>

- *Type:* string

---

###### `props`<sup>Optional</sup> <a name="props" id="cdk-constructs.ThronDockerLambda.metricAll.parameter.props"></a>

- *Type:* aws-cdk-lib.aws_cloudwatch.MetricOptions

---

##### `metricAllConcurrentExecutions` <a name="metricAllConcurrentExecutions" id="cdk-constructs.ThronDockerLambda.metricAllConcurrentExecutions"></a>

```typescript
import { ThronDockerLambda } from 'cdk-constructs'

ThronDockerLambda.metricAllConcurrentExecutions(props?: MetricOptions)
```

Metric for the number of concurrent executions across all Lambdas.

###### `props`<sup>Optional</sup> <a name="props" id="cdk-constructs.ThronDockerLambda.metricAllConcurrentExecutions.parameter.props"></a>

- *Type:* aws-cdk-lib.aws_cloudwatch.MetricOptions

---

##### `metricAllDuration` <a name="metricAllDuration" id="cdk-constructs.ThronDockerLambda.metricAllDuration"></a>

```typescript
import { ThronDockerLambda } from 'cdk-constructs'

ThronDockerLambda.metricAllDuration(props?: MetricOptions)
```

Metric for the Duration executing all Lambdas.

###### `props`<sup>Optional</sup> <a name="props" id="cdk-constructs.ThronDockerLambda.metricAllDuration.parameter.props"></a>

- *Type:* aws-cdk-lib.aws_cloudwatch.MetricOptions

---

##### `metricAllErrors` <a name="metricAllErrors" id="cdk-constructs.ThronDockerLambda.metricAllErrors"></a>

```typescript
import { ThronDockerLambda } from 'cdk-constructs'

ThronDockerLambda.metricAllErrors(props?: MetricOptions)
```

Metric for the number of Errors executing all Lambdas.

###### `props`<sup>Optional</sup> <a name="props" id="cdk-constructs.ThronDockerLambda.metricAllErrors.parameter.props"></a>

- *Type:* aws-cdk-lib.aws_cloudwatch.MetricOptions

---

##### `metricAllInvocations` <a name="metricAllInvocations" id="cdk-constructs.ThronDockerLambda.metricAllInvocations"></a>

```typescript
import { ThronDockerLambda } from 'cdk-constructs'

ThronDockerLambda.metricAllInvocations(props?: MetricOptions)
```

Metric for the number of invocations of all Lambdas.

###### `props`<sup>Optional</sup> <a name="props" id="cdk-constructs.ThronDockerLambda.metricAllInvocations.parameter.props"></a>

- *Type:* aws-cdk-lib.aws_cloudwatch.MetricOptions

---

##### `metricAllThrottles` <a name="metricAllThrottles" id="cdk-constructs.ThronDockerLambda.metricAllThrottles"></a>

```typescript
import { ThronDockerLambda } from 'cdk-constructs'

ThronDockerLambda.metricAllThrottles(props?: MetricOptions)
```

Metric for the number of throttled invocations of all Lambdas.

###### `props`<sup>Optional</sup> <a name="props" id="cdk-constructs.ThronDockerLambda.metricAllThrottles.parameter.props"></a>

- *Type:* aws-cdk-lib.aws_cloudwatch.MetricOptions

---

##### `metricAllUnreservedConcurrentExecutions` <a name="metricAllUnreservedConcurrentExecutions" id="cdk-constructs.ThronDockerLambda.metricAllUnreservedConcurrentExecutions"></a>

```typescript
import { ThronDockerLambda } from 'cdk-constructs'

ThronDockerLambda.metricAllUnreservedConcurrentExecutions(props?: MetricOptions)
```

Metric for the number of unreserved concurrent executions across all Lambdas.

###### `props`<sup>Optional</sup> <a name="props" id="cdk-constructs.ThronDockerLambda.metricAllUnreservedConcurrentExecutions.parameter.props"></a>

- *Type:* aws-cdk-lib.aws_cloudwatch.MetricOptions

---

#### Properties <a name="Properties" id="Properties"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.ThronDockerLambda.property.node">node</a></code> | <code>constructs.Node</code> | The tree node. |
| <code><a href="#cdk-constructs.ThronDockerLambda.property.env">env</a></code> | <code>aws-cdk-lib.ResourceEnvironment</code> | The environment this resource belongs to. |
| <code><a href="#cdk-constructs.ThronDockerLambda.property.stack">stack</a></code> | <code>aws-cdk-lib.Stack</code> | The stack in which this resource is defined. |
| <code><a href="#cdk-constructs.ThronDockerLambda.property.architecture">architecture</a></code> | <code>aws-cdk-lib.aws_lambda.Architecture</code> | The architecture of this Lambda Function (this is an optional attribute and defaults to X86_64). |
| <code><a href="#cdk-constructs.ThronDockerLambda.property.connections">connections</a></code> | <code>aws-cdk-lib.aws_ec2.Connections</code> | Access the Connections object. |
| <code><a href="#cdk-constructs.ThronDockerLambda.property.functionArn">functionArn</a></code> | <code>string</code> | ARN of this function. |
| <code><a href="#cdk-constructs.ThronDockerLambda.property.functionName">functionName</a></code> | <code>string</code> | Name of this function. |
| <code><a href="#cdk-constructs.ThronDockerLambda.property.grantPrincipal">grantPrincipal</a></code> | <code>aws-cdk-lib.aws_iam.IPrincipal</code> | The principal this Lambda Function is running as. |
| <code><a href="#cdk-constructs.ThronDockerLambda.property.isBoundToVpc">isBoundToVpc</a></code> | <code>boolean</code> | Whether or not this Lambda function was bound to a VPC. |
| <code><a href="#cdk-constructs.ThronDockerLambda.property.latestVersion">latestVersion</a></code> | <code>aws-cdk-lib.aws_lambda.IVersion</code> | The `$LATEST` version of this function. |
| <code><a href="#cdk-constructs.ThronDockerLambda.property.permissionsNode">permissionsNode</a></code> | <code>constructs.Node</code> | The construct node where permissions are attached. |
| <code><a href="#cdk-constructs.ThronDockerLambda.property.resourceArnsForGrantInvoke">resourceArnsForGrantInvoke</a></code> | <code>string[]</code> | The ARN(s) to put into the resource field of the generated IAM policy for grantInvoke(). |
| <code><a href="#cdk-constructs.ThronDockerLambda.property.role">role</a></code> | <code>aws-cdk-lib.aws_iam.IRole</code> | Execution role associated with this function. |
| <code><a href="#cdk-constructs.ThronDockerLambda.property.currentVersion">currentVersion</a></code> | <code>aws-cdk-lib.aws_lambda.Version</code> | Returns a `lambda.Version` which represents the current version of this Lambda function. A new version will be created every time the function's configuration changes. |
| <code><a href="#cdk-constructs.ThronDockerLambda.property.logGroup">logGroup</a></code> | <code>aws-cdk-lib.aws_logs.ILogGroup</code> | The LogGroup where the Lambda function's logs are made available. |
| <code><a href="#cdk-constructs.ThronDockerLambda.property.runtime">runtime</a></code> | <code>aws-cdk-lib.aws_lambda.Runtime</code> | The runtime configured for this lambda. |
| <code><a href="#cdk-constructs.ThronDockerLambda.property.deadLetterQueue">deadLetterQueue</a></code> | <code>aws-cdk-lib.aws_sqs.IQueue</code> | The DLQ (as queue) associated with this Lambda Function (this is an optional attribute). |
| <code><a href="#cdk-constructs.ThronDockerLambda.property.deadLetterTopic">deadLetterTopic</a></code> | <code>aws-cdk-lib.aws_sns.ITopic</code> | The DLQ (as topic) associated with this Lambda Function (this is an optional attribute). |
| <code><a href="#cdk-constructs.ThronDockerLambda.property.timeout">timeout</a></code> | <code>aws-cdk-lib.Duration</code> | The timeout configured for this lambda. |
| <code><a href="#cdk-constructs.ThronDockerLambda.property.apiGatewayEndpoints">apiGatewayEndpoints</a></code> | <code>{[ key: string ]: <a href="#cdk-constructs.ThronCreatedApiGatewayEndpoint">ThronCreatedApiGatewayEndpoint</a>}</code> | *No description.* |
| <code><a href="#cdk-constructs.ThronDockerLambda.property.endpoints">endpoints</a></code> | <code>{[ key: string ]: <a href="#cdk-constructs.EndpointAlb">EndpointAlb</a>}</code> | *No description.* |
| <code><a href="#cdk-constructs.ThronDockerLambda.property.legacyEndpoints">legacyEndpoints</a></code> | <code>{[ key: string ]: <a href="#cdk-constructs.EndpointAlb">EndpointAlb</a>}</code> | *No description.* |

---

##### `node`<sup>Required</sup> <a name="node" id="cdk-constructs.ThronDockerLambda.property.node"></a>

```typescript
public readonly node: Node;
```

- *Type:* constructs.Node

The tree node.

---

##### `env`<sup>Required</sup> <a name="env" id="cdk-constructs.ThronDockerLambda.property.env"></a>

```typescript
public readonly env: ResourceEnvironment;
```

- *Type:* aws-cdk-lib.ResourceEnvironment

The environment this resource belongs to.

For resources that are created and managed by the CDK
(generally, those created by creating new class instances like Role, Bucket, etc.),
this is always the same as the environment of the stack they belong to;
however, for imported resources
(those obtained from static methods like fromRoleArn, fromBucketName, etc.),
that might be different than the stack they were imported into.

---

##### `stack`<sup>Required</sup> <a name="stack" id="cdk-constructs.ThronDockerLambda.property.stack"></a>

```typescript
public readonly stack: Stack;
```

- *Type:* aws-cdk-lib.Stack

The stack in which this resource is defined.

---

##### `architecture`<sup>Required</sup> <a name="architecture" id="cdk-constructs.ThronDockerLambda.property.architecture"></a>

```typescript
public readonly architecture: Architecture;
```

- *Type:* aws-cdk-lib.aws_lambda.Architecture

The architecture of this Lambda Function (this is an optional attribute and defaults to X86_64).

---

##### `connections`<sup>Required</sup> <a name="connections" id="cdk-constructs.ThronDockerLambda.property.connections"></a>

```typescript
public readonly connections: Connections;
```

- *Type:* aws-cdk-lib.aws_ec2.Connections

Access the Connections object.

Will fail if not a VPC-enabled Lambda Function

---

##### `functionArn`<sup>Required</sup> <a name="functionArn" id="cdk-constructs.ThronDockerLambda.property.functionArn"></a>

```typescript
public readonly functionArn: string;
```

- *Type:* string

ARN of this function.

---

##### `functionName`<sup>Required</sup> <a name="functionName" id="cdk-constructs.ThronDockerLambda.property.functionName"></a>

```typescript
public readonly functionName: string;
```

- *Type:* string

Name of this function.

---

##### `grantPrincipal`<sup>Required</sup> <a name="grantPrincipal" id="cdk-constructs.ThronDockerLambda.property.grantPrincipal"></a>

```typescript
public readonly grantPrincipal: IPrincipal;
```

- *Type:* aws-cdk-lib.aws_iam.IPrincipal

The principal this Lambda Function is running as.

---

##### `isBoundToVpc`<sup>Required</sup> <a name="isBoundToVpc" id="cdk-constructs.ThronDockerLambda.property.isBoundToVpc"></a>

```typescript
public readonly isBoundToVpc: boolean;
```

- *Type:* boolean

Whether or not this Lambda function was bound to a VPC.

If this is is `false`, trying to access the `connections` object will fail.

---

##### `latestVersion`<sup>Required</sup> <a name="latestVersion" id="cdk-constructs.ThronDockerLambda.property.latestVersion"></a>

```typescript
public readonly latestVersion: IVersion;
```

- *Type:* aws-cdk-lib.aws_lambda.IVersion

The `$LATEST` version of this function.

Note that this is reference to a non-specific AWS Lambda version, which
means the function this version refers to can return different results in
different invocations.

To obtain a reference to an explicit version which references the current
function configuration, use `lambdaFunction.currentVersion` instead.

---

##### `permissionsNode`<sup>Required</sup> <a name="permissionsNode" id="cdk-constructs.ThronDockerLambda.property.permissionsNode"></a>

```typescript
public readonly permissionsNode: Node;
```

- *Type:* constructs.Node

The construct node where permissions are attached.

---

##### `resourceArnsForGrantInvoke`<sup>Required</sup> <a name="resourceArnsForGrantInvoke" id="cdk-constructs.ThronDockerLambda.property.resourceArnsForGrantInvoke"></a>

```typescript
public readonly resourceArnsForGrantInvoke: string[];
```

- *Type:* string[]

The ARN(s) to put into the resource field of the generated IAM policy for grantInvoke().

---

##### `role`<sup>Optional</sup> <a name="role" id="cdk-constructs.ThronDockerLambda.property.role"></a>

```typescript
public readonly role: IRole;
```

- *Type:* aws-cdk-lib.aws_iam.IRole

Execution role associated with this function.

---

##### `currentVersion`<sup>Required</sup> <a name="currentVersion" id="cdk-constructs.ThronDockerLambda.property.currentVersion"></a>

```typescript
public readonly currentVersion: Version;
```

- *Type:* aws-cdk-lib.aws_lambda.Version

Returns a `lambda.Version` which represents the current version of this Lambda function. A new version will be created every time the function's configuration changes.

You can specify options for this version using the `currentVersionOptions`
prop when initializing the `lambda.Function`.

---

##### `logGroup`<sup>Required</sup> <a name="logGroup" id="cdk-constructs.ThronDockerLambda.property.logGroup"></a>

```typescript
public readonly logGroup: ILogGroup;
```

- *Type:* aws-cdk-lib.aws_logs.ILogGroup

The LogGroup where the Lambda function's logs are made available.

If either `logRetention` is set or this property is called, a CloudFormation custom resource is added to the stack that
pre-creates the log group as part of the stack deployment, if it already doesn't exist, and sets the correct log retention
period (never expire, by default).

Further, if the log group already exists and the `logRetention` is not set, the custom resource will reset the log retention
to never expire even if it was configured with a different value.

---

##### `runtime`<sup>Required</sup> <a name="runtime" id="cdk-constructs.ThronDockerLambda.property.runtime"></a>

```typescript
public readonly runtime: Runtime;
```

- *Type:* aws-cdk-lib.aws_lambda.Runtime

The runtime configured for this lambda.

---

##### `deadLetterQueue`<sup>Optional</sup> <a name="deadLetterQueue" id="cdk-constructs.ThronDockerLambda.property.deadLetterQueue"></a>

```typescript
public readonly deadLetterQueue: IQueue;
```

- *Type:* aws-cdk-lib.aws_sqs.IQueue

The DLQ (as queue) associated with this Lambda Function (this is an optional attribute).

---

##### `deadLetterTopic`<sup>Optional</sup> <a name="deadLetterTopic" id="cdk-constructs.ThronDockerLambda.property.deadLetterTopic"></a>

```typescript
public readonly deadLetterTopic: ITopic;
```

- *Type:* aws-cdk-lib.aws_sns.ITopic

The DLQ (as topic) associated with this Lambda Function (this is an optional attribute).

---

##### `timeout`<sup>Optional</sup> <a name="timeout" id="cdk-constructs.ThronDockerLambda.property.timeout"></a>

```typescript
public readonly timeout: Duration;
```

- *Type:* aws-cdk-lib.Duration

The timeout configured for this lambda.

---

##### `apiGatewayEndpoints`<sup>Optional</sup> <a name="apiGatewayEndpoints" id="cdk-constructs.ThronDockerLambda.property.apiGatewayEndpoints"></a>

```typescript
public readonly apiGatewayEndpoints: {[ key: string ]: ThronCreatedApiGatewayEndpoint};
```

- *Type:* {[ key: string ]: <a href="#cdk-constructs.ThronCreatedApiGatewayEndpoint">ThronCreatedApiGatewayEndpoint</a>}

---

##### `endpoints`<sup>Optional</sup> <a name="endpoints" id="cdk-constructs.ThronDockerLambda.property.endpoints"></a>

```typescript
public readonly endpoints: {[ key: string ]: EndpointAlb};
```

- *Type:* {[ key: string ]: <a href="#cdk-constructs.EndpointAlb">EndpointAlb</a>}

---

##### `legacyEndpoints`<sup>Optional</sup> <a name="legacyEndpoints" id="cdk-constructs.ThronDockerLambda.property.legacyEndpoints"></a>

```typescript
public readonly legacyEndpoints: {[ key: string ]: EndpointAlb};
```

- *Type:* {[ key: string ]: <a href="#cdk-constructs.EndpointAlb">EndpointAlb</a>}

---


### ThronEc2Service <a name="ThronEc2Service" id="cdk-constructs.ThronEc2Service"></a>

#### Initializers <a name="Initializers" id="cdk-constructs.ThronEc2Service.Initializer"></a>

```typescript
import { ThronEc2Service } from 'cdk-constructs'

new ThronEc2Service(scope: Stack, id: string, props: ThronEc2ServiceProps)
```

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.ThronEc2Service.Initializer.parameter.scope">scope</a></code> | <code>aws-cdk-lib.Stack</code> | *No description.* |
| <code><a href="#cdk-constructs.ThronEc2Service.Initializer.parameter.id">id</a></code> | <code>string</code> | *No description.* |
| <code><a href="#cdk-constructs.ThronEc2Service.Initializer.parameter.props">props</a></code> | <code><a href="#cdk-constructs.ThronEc2ServiceProps">ThronEc2ServiceProps</a></code> | *No description.* |

---

##### `scope`<sup>Required</sup> <a name="scope" id="cdk-constructs.ThronEc2Service.Initializer.parameter.scope"></a>

- *Type:* aws-cdk-lib.Stack

---

##### `id`<sup>Required</sup> <a name="id" id="cdk-constructs.ThronEc2Service.Initializer.parameter.id"></a>

- *Type:* string

---

##### `props`<sup>Required</sup> <a name="props" id="cdk-constructs.ThronEc2Service.Initializer.parameter.props"></a>

- *Type:* <a href="#cdk-constructs.ThronEc2ServiceProps">ThronEc2ServiceProps</a>

---

#### Methods <a name="Methods" id="Methods"></a>

| **Name** | **Description** |
| --- | --- |
| <code><a href="#cdk-constructs.ThronEc2Service.toString">toString</a></code> | Returns a string representation of this construct. |
| <code><a href="#cdk-constructs.ThronEc2Service.applyRemovalPolicy">applyRemovalPolicy</a></code> | Apply the given removal policy to this resource. |
| <code><a href="#cdk-constructs.ThronEc2Service.addVolume">addVolume</a></code> | Adds a volume to the Service. |
| <code><a href="#cdk-constructs.ThronEc2Service.associateCloudMapService">associateCloudMapService</a></code> | Associates this service with a CloudMap service. |
| <code><a href="#cdk-constructs.ThronEc2Service.attachToApplicationTargetGroup">attachToApplicationTargetGroup</a></code> | This method is called to attach this service to an Application Load Balancer. |
| <code><a href="#cdk-constructs.ThronEc2Service.attachToClassicLB">attachToClassicLB</a></code> | Registers the service as a target of a Classic Load Balancer (CLB). |
| <code><a href="#cdk-constructs.ThronEc2Service.attachToNetworkTargetGroup">attachToNetworkTargetGroup</a></code> | This method is called to attach this service to a Network Load Balancer. |
| <code><a href="#cdk-constructs.ThronEc2Service.autoScaleTaskCount">autoScaleTaskCount</a></code> | An attribute representing the minimum and maximum task count for an AutoScalingGroup. |
| <code><a href="#cdk-constructs.ThronEc2Service.enableCloudMap">enableCloudMap</a></code> | Enable CloudMap service discovery for the service. |
| <code><a href="#cdk-constructs.ThronEc2Service.enableDeploymentAlarms">enableDeploymentAlarms</a></code> | Enable Deployment Alarms which take advantage of arbitrary alarms and configure them after service initialization. |
| <code><a href="#cdk-constructs.ThronEc2Service.enableServiceConnect">enableServiceConnect</a></code> | Enable Service Connect on this service. |
| <code><a href="#cdk-constructs.ThronEc2Service.loadBalancerTarget">loadBalancerTarget</a></code> | Return a load balancing target for a specific container and port. |
| <code><a href="#cdk-constructs.ThronEc2Service.metric">metric</a></code> | This method returns the specified CloudWatch metric name for this service. |
| <code><a href="#cdk-constructs.ThronEc2Service.metricCpuUtilization">metricCpuUtilization</a></code> | This method returns the CloudWatch metric for this service's CPU utilization. |
| <code><a href="#cdk-constructs.ThronEc2Service.metricMemoryUtilization">metricMemoryUtilization</a></code> | This method returns the CloudWatch metric for this service's memory utilization. |
| <code><a href="#cdk-constructs.ThronEc2Service.registerLoadBalancerTargets">registerLoadBalancerTargets</a></code> | Use this function to create all load balancer targets to be registered in this service, add them to target groups, and attach target groups to listeners accordingly. |
| <code><a href="#cdk-constructs.ThronEc2Service.addPlacementConstraints">addPlacementConstraints</a></code> | Adds one or more placement constraints to use for tasks in the service. |
| <code><a href="#cdk-constructs.ThronEc2Service.addPlacementStrategies">addPlacementStrategies</a></code> | Adds one or more placement strategies to use for tasks in the service. |
| <code><a href="#cdk-constructs.ThronEc2Service.addEndpointAlb">addEndpointAlb</a></code> | Add an endpoint for the EC2 service. |
| <code><a href="#cdk-constructs.ThronEc2Service.addLegacyEndpointAlb">addLegacyEndpointAlb</a></code> | Add a legacy endpoint for the EC2 service. |
| <code><a href="#cdk-constructs.ThronEc2Service.addTargetScaling">addTargetScaling</a></code> | Configures an EC2 service as a scalable target. |

---

##### `toString` <a name="toString" id="cdk-constructs.ThronEc2Service.toString"></a>

```typescript
public toString(): string
```

Returns a string representation of this construct.

##### `applyRemovalPolicy` <a name="applyRemovalPolicy" id="cdk-constructs.ThronEc2Service.applyRemovalPolicy"></a>

```typescript
public applyRemovalPolicy(policy: RemovalPolicy): void
```

Apply the given removal policy to this resource.

The Removal Policy controls what happens to this resource when it stops
being managed by CloudFormation, either because you've removed it from the
CDK application or because you've made a change that requires the resource
to be replaced.

The resource can be deleted (`RemovalPolicy.DESTROY`), or left in your AWS
account for data recovery and cleanup later (`RemovalPolicy.RETAIN`).

###### `policy`<sup>Required</sup> <a name="policy" id="cdk-constructs.ThronEc2Service.applyRemovalPolicy.parameter.policy"></a>

- *Type:* aws-cdk-lib.RemovalPolicy

---

##### `addVolume` <a name="addVolume" id="cdk-constructs.ThronEc2Service.addVolume"></a>

```typescript
public addVolume(volume: ServiceManagedVolume): void
```

Adds a volume to the Service.

###### `volume`<sup>Required</sup> <a name="volume" id="cdk-constructs.ThronEc2Service.addVolume.parameter.volume"></a>

- *Type:* aws-cdk-lib.aws_ecs.ServiceManagedVolume

---

##### `associateCloudMapService` <a name="associateCloudMapService" id="cdk-constructs.ThronEc2Service.associateCloudMapService"></a>

```typescript
public associateCloudMapService(options: AssociateCloudMapServiceOptions): void
```

Associates this service with a CloudMap service.

###### `options`<sup>Required</sup> <a name="options" id="cdk-constructs.ThronEc2Service.associateCloudMapService.parameter.options"></a>

- *Type:* aws-cdk-lib.aws_ecs.AssociateCloudMapServiceOptions

---

##### `attachToApplicationTargetGroup` <a name="attachToApplicationTargetGroup" id="cdk-constructs.ThronEc2Service.attachToApplicationTargetGroup"></a>

```typescript
public attachToApplicationTargetGroup(targetGroup: IApplicationTargetGroup): LoadBalancerTargetProps
```

This method is called to attach this service to an Application Load Balancer.

Don't call this function directly. Instead, call `listener.addTargets()`
to add this service to a load balancer.

###### `targetGroup`<sup>Required</sup> <a name="targetGroup" id="cdk-constructs.ThronEc2Service.attachToApplicationTargetGroup.parameter.targetGroup"></a>

- *Type:* aws-cdk-lib.aws_elasticloadbalancingv2.IApplicationTargetGroup

---

##### `attachToClassicLB` <a name="attachToClassicLB" id="cdk-constructs.ThronEc2Service.attachToClassicLB"></a>

```typescript
public attachToClassicLB(loadBalancer: LoadBalancer): void
```

Registers the service as a target of a Classic Load Balancer (CLB).

Don't call this. Call `loadBalancer.addTarget()` instead.

###### `loadBalancer`<sup>Required</sup> <a name="loadBalancer" id="cdk-constructs.ThronEc2Service.attachToClassicLB.parameter.loadBalancer"></a>

- *Type:* aws-cdk-lib.aws_elasticloadbalancing.LoadBalancer

---

##### `attachToNetworkTargetGroup` <a name="attachToNetworkTargetGroup" id="cdk-constructs.ThronEc2Service.attachToNetworkTargetGroup"></a>

```typescript
public attachToNetworkTargetGroup(targetGroup: INetworkTargetGroup): LoadBalancerTargetProps
```

This method is called to attach this service to a Network Load Balancer.

Don't call this function directly. Instead, call `listener.addTargets()`
to add this service to a load balancer.

###### `targetGroup`<sup>Required</sup> <a name="targetGroup" id="cdk-constructs.ThronEc2Service.attachToNetworkTargetGroup.parameter.targetGroup"></a>

- *Type:* aws-cdk-lib.aws_elasticloadbalancingv2.INetworkTargetGroup

---

##### `autoScaleTaskCount` <a name="autoScaleTaskCount" id="cdk-constructs.ThronEc2Service.autoScaleTaskCount"></a>

```typescript
public autoScaleTaskCount(props: EnableScalingProps): ScalableTaskCount
```

An attribute representing the minimum and maximum task count for an AutoScalingGroup.

###### `props`<sup>Required</sup> <a name="props" id="cdk-constructs.ThronEc2Service.autoScaleTaskCount.parameter.props"></a>

- *Type:* aws-cdk-lib.aws_applicationautoscaling.EnableScalingProps

---

##### `enableCloudMap` <a name="enableCloudMap" id="cdk-constructs.ThronEc2Service.enableCloudMap"></a>

```typescript
public enableCloudMap(options: CloudMapOptions): Service
```

Enable CloudMap service discovery for the service.

###### `options`<sup>Required</sup> <a name="options" id="cdk-constructs.ThronEc2Service.enableCloudMap.parameter.options"></a>

- *Type:* aws-cdk-lib.aws_ecs.CloudMapOptions

---

##### `enableDeploymentAlarms` <a name="enableDeploymentAlarms" id="cdk-constructs.ThronEc2Service.enableDeploymentAlarms"></a>

```typescript
public enableDeploymentAlarms(alarmNames: string[], options?: DeploymentAlarmOptions): void
```

Enable Deployment Alarms which take advantage of arbitrary alarms and configure them after service initialization.

If you have already enabled deployment alarms, this function can be used to tell ECS about additional alarms that
should interrupt a deployment.

New alarms specified in subsequent calls of this function will be appended to the existing list of alarms.

The same Alarm Behavior must be used on all deployment alarms. If you specify different AlarmBehavior values in
multiple calls to this function, or the Alarm Behavior used here doesn't match the one used in the service
constructor, an error will be thrown.

If the alarm's metric references the service, you cannot pass `Alarm.alarmName` here. That will cause a circular
dependency between the service and its deployment alarm. See this package's README for options to alarm on service
metrics, and avoid this circular dependency.

###### `alarmNames`<sup>Required</sup> <a name="alarmNames" id="cdk-constructs.ThronEc2Service.enableDeploymentAlarms.parameter.alarmNames"></a>

- *Type:* string[]

---

###### `options`<sup>Optional</sup> <a name="options" id="cdk-constructs.ThronEc2Service.enableDeploymentAlarms.parameter.options"></a>

- *Type:* aws-cdk-lib.aws_ecs.DeploymentAlarmOptions

---

##### `enableServiceConnect` <a name="enableServiceConnect" id="cdk-constructs.ThronEc2Service.enableServiceConnect"></a>

```typescript
public enableServiceConnect(config?: ServiceConnectProps): void
```

Enable Service Connect on this service.

###### `config`<sup>Optional</sup> <a name="config" id="cdk-constructs.ThronEc2Service.enableServiceConnect.parameter.config"></a>

- *Type:* aws-cdk-lib.aws_ecs.ServiceConnectProps

---

##### `loadBalancerTarget` <a name="loadBalancerTarget" id="cdk-constructs.ThronEc2Service.loadBalancerTarget"></a>

```typescript
public loadBalancerTarget(options: LoadBalancerTargetOptions): IEcsLoadBalancerTarget
```

Return a load balancing target for a specific container and port.

Use this function to create a load balancer target if you want to load balance to
another container than the first essential container or the first mapped port on
the container.

Use the return value of this function where you would normally use a load balancer
target, instead of the `Service` object itself.

*Example*

```typescript
declare const listener: elbv2.ApplicationListener;
declare const service: ecs.BaseService;
listener.addTargets('ECS', {
  port: 80,
  targets: [service.loadBalancerTarget({
    containerName: 'MyContainer',
    containerPort: 1234,
  })],
});
```


###### `options`<sup>Required</sup> <a name="options" id="cdk-constructs.ThronEc2Service.loadBalancerTarget.parameter.options"></a>

- *Type:* aws-cdk-lib.aws_ecs.LoadBalancerTargetOptions

---

##### `metric` <a name="metric" id="cdk-constructs.ThronEc2Service.metric"></a>

```typescript
public metric(metricName: string, props?: MetricOptions): Metric
```

This method returns the specified CloudWatch metric name for this service.

###### `metricName`<sup>Required</sup> <a name="metricName" id="cdk-constructs.ThronEc2Service.metric.parameter.metricName"></a>

- *Type:* string

---

###### `props`<sup>Optional</sup> <a name="props" id="cdk-constructs.ThronEc2Service.metric.parameter.props"></a>

- *Type:* aws-cdk-lib.aws_cloudwatch.MetricOptions

---

##### `metricCpuUtilization` <a name="metricCpuUtilization" id="cdk-constructs.ThronEc2Service.metricCpuUtilization"></a>

```typescript
public metricCpuUtilization(props?: MetricOptions): Metric
```

This method returns the CloudWatch metric for this service's CPU utilization.

###### `props`<sup>Optional</sup> <a name="props" id="cdk-constructs.ThronEc2Service.metricCpuUtilization.parameter.props"></a>

- *Type:* aws-cdk-lib.aws_cloudwatch.MetricOptions

---

##### `metricMemoryUtilization` <a name="metricMemoryUtilization" id="cdk-constructs.ThronEc2Service.metricMemoryUtilization"></a>

```typescript
public metricMemoryUtilization(props?: MetricOptions): Metric
```

This method returns the CloudWatch metric for this service's memory utilization.

###### `props`<sup>Optional</sup> <a name="props" id="cdk-constructs.ThronEc2Service.metricMemoryUtilization.parameter.props"></a>

- *Type:* aws-cdk-lib.aws_cloudwatch.MetricOptions

---

##### `registerLoadBalancerTargets` <a name="registerLoadBalancerTargets" id="cdk-constructs.ThronEc2Service.registerLoadBalancerTargets"></a>

```typescript
public registerLoadBalancerTargets(targets: EcsTarget): void
```

Use this function to create all load balancer targets to be registered in this service, add them to target groups, and attach target groups to listeners accordingly.

Alternatively, you can use `listener.addTargets()` to create targets and add them to target groups.

*Example*

```typescript
declare const listener: elbv2.ApplicationListener;
declare const service: ecs.BaseService;
service.registerLoadBalancerTargets(
  {
    containerName: 'web',
    containerPort: 80,
    newTargetGroupId: 'ECS',
    listener: ecs.ListenerConfig.applicationListener(listener, {
      protocol: elbv2.ApplicationProtocol.HTTPS
    }),
  },
)
```


###### `targets`<sup>Required</sup> <a name="targets" id="cdk-constructs.ThronEc2Service.registerLoadBalancerTargets.parameter.targets"></a>

- *Type:* aws-cdk-lib.aws_ecs.EcsTarget

---

##### `addPlacementConstraints` <a name="addPlacementConstraints" id="cdk-constructs.ThronEc2Service.addPlacementConstraints"></a>

```typescript
public addPlacementConstraints(constraints: PlacementConstraint): void
```

Adds one or more placement constraints to use for tasks in the service.

For more information, see
[Amazon ECS Task Placement Constraints](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/task-placement-constraints.html).

###### `constraints`<sup>Required</sup> <a name="constraints" id="cdk-constructs.ThronEc2Service.addPlacementConstraints.parameter.constraints"></a>

- *Type:* aws-cdk-lib.aws_ecs.PlacementConstraint

---

##### `addPlacementStrategies` <a name="addPlacementStrategies" id="cdk-constructs.ThronEc2Service.addPlacementStrategies"></a>

```typescript
public addPlacementStrategies(strategies: PlacementStrategy): void
```

Adds one or more placement strategies to use for tasks in the service.

For more information, see
[Amazon ECS Task Placement Strategies](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/task-placement-strategies.html).

###### `strategies`<sup>Required</sup> <a name="strategies" id="cdk-constructs.ThronEc2Service.addPlacementStrategies.parameter.strategies"></a>

- *Type:* aws-cdk-lib.aws_ecs.PlacementStrategy

---

##### `addEndpointAlb` <a name="addEndpointAlb" id="cdk-constructs.ThronEc2Service.addEndpointAlb"></a>

```typescript
public addEndpointAlb(name: string, endpointProps: ThronEndpointAlbProps): EndpointAlb
```

Add an endpoint for the EC2 service.

###### `name`<sup>Required</sup> <a name="name" id="cdk-constructs.ThronEc2Service.addEndpointAlb.parameter.name"></a>

- *Type:* string

---

###### `endpointProps`<sup>Required</sup> <a name="endpointProps" id="cdk-constructs.ThronEc2Service.addEndpointAlb.parameter.endpointProps"></a>

- *Type:* <a href="#cdk-constructs.ThronEndpointAlbProps">ThronEndpointAlbProps</a>

---

##### `addLegacyEndpointAlb` <a name="addLegacyEndpointAlb" id="cdk-constructs.ThronEc2Service.addLegacyEndpointAlb"></a>

```typescript
public addLegacyEndpointAlb(name: string, endpointProps: LegacyEndpointAlbProps): EndpointAlb
```

Add a legacy endpoint for the EC2 service.

###### `name`<sup>Required</sup> <a name="name" id="cdk-constructs.ThronEc2Service.addLegacyEndpointAlb.parameter.name"></a>

- *Type:* string

---

###### `endpointProps`<sup>Required</sup> <a name="endpointProps" id="cdk-constructs.ThronEc2Service.addLegacyEndpointAlb.parameter.endpointProps"></a>

- *Type:* <a href="#cdk-constructs.LegacyEndpointAlbProps">LegacyEndpointAlbProps</a>

---

##### `addTargetScaling` <a name="addTargetScaling" id="cdk-constructs.ThronEc2Service.addTargetScaling"></a>

```typescript
public addTargetScaling(targetScaling: ThronTargetScalingProps): ThronEc2TargetScaling
```

Configures an EC2 service as a scalable target.

###### `targetScaling`<sup>Required</sup> <a name="targetScaling" id="cdk-constructs.ThronEc2Service.addTargetScaling.parameter.targetScaling"></a>

- *Type:* <a href="#cdk-constructs.ThronTargetScalingProps">ThronTargetScalingProps</a>

target scaling property.

---

#### Static Functions <a name="Static Functions" id="Static Functions"></a>

| **Name** | **Description** |
| --- | --- |
| <code><a href="#cdk-constructs.ThronEc2Service.isConstruct">isConstruct</a></code> | Checks if `x` is a construct. |
| <code><a href="#cdk-constructs.ThronEc2Service.isOwnedResource">isOwnedResource</a></code> | Returns true if the construct was created by CDK, and false otherwise. |
| <code><a href="#cdk-constructs.ThronEc2Service.isResource">isResource</a></code> | Check whether the given construct is a Resource. |
| <code><a href="#cdk-constructs.ThronEc2Service.fromServiceArnWithCluster">fromServiceArnWithCluster</a></code> | Import an existing ECS/Fargate Service using the service cluster format. |
| <code><a href="#cdk-constructs.ThronEc2Service.fromEc2ServiceArn">fromEc2ServiceArn</a></code> | Imports from the specified service ARN. |
| <code><a href="#cdk-constructs.ThronEc2Service.fromEc2ServiceAttributes">fromEc2ServiceAttributes</a></code> | Imports from the specified service attributes. |

---

##### `isConstruct` <a name="isConstruct" id="cdk-constructs.ThronEc2Service.isConstruct"></a>

```typescript
import { ThronEc2Service } from 'cdk-constructs'

ThronEc2Service.isConstruct(x: any)
```

Checks if `x` is a construct.

Use this method instead of `instanceof` to properly detect `Construct`
instances, even when the construct library is symlinked.

Explanation: in JavaScript, multiple copies of the `constructs` library on
disk are seen as independent, completely different libraries. As a
consequence, the class `Construct` in each copy of the `constructs` library
is seen as a different class, and an instance of one class will not test as
`instanceof` the other class. `npm install` will not create installations
like this, but users may manually symlink construct libraries together or
use a monorepo tool: in those cases, multiple copies of the `constructs`
library can be accidentally installed, and `instanceof` will behave
unpredictably. It is safest to avoid using `instanceof`, and using
this type-testing method instead.

###### `x`<sup>Required</sup> <a name="x" id="cdk-constructs.ThronEc2Service.isConstruct.parameter.x"></a>

- *Type:* any

Any object.

---

##### `isOwnedResource` <a name="isOwnedResource" id="cdk-constructs.ThronEc2Service.isOwnedResource"></a>

```typescript
import { ThronEc2Service } from 'cdk-constructs'

ThronEc2Service.isOwnedResource(construct: IConstruct)
```

Returns true if the construct was created by CDK, and false otherwise.

###### `construct`<sup>Required</sup> <a name="construct" id="cdk-constructs.ThronEc2Service.isOwnedResource.parameter.construct"></a>

- *Type:* constructs.IConstruct

---

##### `isResource` <a name="isResource" id="cdk-constructs.ThronEc2Service.isResource"></a>

```typescript
import { ThronEc2Service } from 'cdk-constructs'

ThronEc2Service.isResource(construct: IConstruct)
```

Check whether the given construct is a Resource.

###### `construct`<sup>Required</sup> <a name="construct" id="cdk-constructs.ThronEc2Service.isResource.parameter.construct"></a>

- *Type:* constructs.IConstruct

---

##### `fromServiceArnWithCluster` <a name="fromServiceArnWithCluster" id="cdk-constructs.ThronEc2Service.fromServiceArnWithCluster"></a>

```typescript
import { ThronEc2Service } from 'cdk-constructs'

ThronEc2Service.fromServiceArnWithCluster(scope: Construct, id: string, serviceArn: string)
```

Import an existing ECS/Fargate Service using the service cluster format.

The format is the "new" format "arn:aws:ecs:region:aws_account_id:service/cluster-name/service-name".

> [https://docs.aws.amazon.com/AmazonECS/latest/developerguide/ecs-account-settings.html#ecs-resource-ids](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/ecs-account-settings.html#ecs-resource-ids)

###### `scope`<sup>Required</sup> <a name="scope" id="cdk-constructs.ThronEc2Service.fromServiceArnWithCluster.parameter.scope"></a>

- *Type:* constructs.Construct

---

###### `id`<sup>Required</sup> <a name="id" id="cdk-constructs.ThronEc2Service.fromServiceArnWithCluster.parameter.id"></a>

- *Type:* string

---

###### `serviceArn`<sup>Required</sup> <a name="serviceArn" id="cdk-constructs.ThronEc2Service.fromServiceArnWithCluster.parameter.serviceArn"></a>

- *Type:* string

---

##### `fromEc2ServiceArn` <a name="fromEc2ServiceArn" id="cdk-constructs.ThronEc2Service.fromEc2ServiceArn"></a>

```typescript
import { ThronEc2Service } from 'cdk-constructs'

ThronEc2Service.fromEc2ServiceArn(scope: Construct, id: string, ec2ServiceArn: string)
```

Imports from the specified service ARN.

###### `scope`<sup>Required</sup> <a name="scope" id="cdk-constructs.ThronEc2Service.fromEc2ServiceArn.parameter.scope"></a>

- *Type:* constructs.Construct

---

###### `id`<sup>Required</sup> <a name="id" id="cdk-constructs.ThronEc2Service.fromEc2ServiceArn.parameter.id"></a>

- *Type:* string

---

###### `ec2ServiceArn`<sup>Required</sup> <a name="ec2ServiceArn" id="cdk-constructs.ThronEc2Service.fromEc2ServiceArn.parameter.ec2ServiceArn"></a>

- *Type:* string

---

##### `fromEc2ServiceAttributes` <a name="fromEc2ServiceAttributes" id="cdk-constructs.ThronEc2Service.fromEc2ServiceAttributes"></a>

```typescript
import { ThronEc2Service } from 'cdk-constructs'

ThronEc2Service.fromEc2ServiceAttributes(scope: Construct, id: string, attrs: Ec2ServiceAttributes)
```

Imports from the specified service attributes.

###### `scope`<sup>Required</sup> <a name="scope" id="cdk-constructs.ThronEc2Service.fromEc2ServiceAttributes.parameter.scope"></a>

- *Type:* constructs.Construct

---

###### `id`<sup>Required</sup> <a name="id" id="cdk-constructs.ThronEc2Service.fromEc2ServiceAttributes.parameter.id"></a>

- *Type:* string

---

###### `attrs`<sup>Required</sup> <a name="attrs" id="cdk-constructs.ThronEc2Service.fromEc2ServiceAttributes.parameter.attrs"></a>

- *Type:* aws-cdk-lib.aws_ecs.Ec2ServiceAttributes

---

#### Properties <a name="Properties" id="Properties"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.ThronEc2Service.property.node">node</a></code> | <code>constructs.Node</code> | The tree node. |
| <code><a href="#cdk-constructs.ThronEc2Service.property.env">env</a></code> | <code>aws-cdk-lib.ResourceEnvironment</code> | The environment this resource belongs to. |
| <code><a href="#cdk-constructs.ThronEc2Service.property.stack">stack</a></code> | <code>aws-cdk-lib.Stack</code> | The stack in which this resource is defined. |
| <code><a href="#cdk-constructs.ThronEc2Service.property.cluster">cluster</a></code> | <code>aws-cdk-lib.aws_ecs.ICluster</code> | The cluster that hosts the service. |
| <code><a href="#cdk-constructs.ThronEc2Service.property.connections">connections</a></code> | <code>aws-cdk-lib.aws_ec2.Connections</code> | The security groups which manage the allowed network traffic for the service. |
| <code><a href="#cdk-constructs.ThronEc2Service.property.serviceArn">serviceArn</a></code> | <code>string</code> | The Amazon Resource Name (ARN) of the service. |
| <code><a href="#cdk-constructs.ThronEc2Service.property.serviceName">serviceName</a></code> | <code>string</code> | The name of the service. |
| <code><a href="#cdk-constructs.ThronEc2Service.property.taskDefinition">taskDefinition</a></code> | <code>aws-cdk-lib.aws_ecs.TaskDefinition</code> | The task definition to use for tasks in the service. |
| <code><a href="#cdk-constructs.ThronEc2Service.property.cloudMapService">cloudMapService</a></code> | <code>aws-cdk-lib.aws_servicediscovery.IService</code> | The CloudMap service created for this service, if any. |
| <code><a href="#cdk-constructs.ThronEc2Service.property.ec2TaskDefinition">ec2TaskDefinition</a></code> | <code><a href="#cdk-constructs.ThronEc2TaskDefinition">ThronEc2TaskDefinition</a></code> | *No description.* |
| <code><a href="#cdk-constructs.ThronEc2Service.property.endpoints">endpoints</a></code> | <code>{[ key: string ]: <a href="#cdk-constructs.EndpointAlb">EndpointAlb</a>}</code> | *No description.* |
| <code><a href="#cdk-constructs.ThronEc2Service.property.legacyEndpoints">legacyEndpoints</a></code> | <code>{[ key: string ]: <a href="#cdk-constructs.EndpointAlb">EndpointAlb</a>}</code> | *No description.* |
| <code><a href="#cdk-constructs.ThronEc2Service.property.targetScaling">targetScaling</a></code> | <code><a href="#cdk-constructs.ThronTargetScaling">ThronTargetScaling</a></code> | *No description.* |

---

##### `node`<sup>Required</sup> <a name="node" id="cdk-constructs.ThronEc2Service.property.node"></a>

```typescript
public readonly node: Node;
```

- *Type:* constructs.Node

The tree node.

---

##### `env`<sup>Required</sup> <a name="env" id="cdk-constructs.ThronEc2Service.property.env"></a>

```typescript
public readonly env: ResourceEnvironment;
```

- *Type:* aws-cdk-lib.ResourceEnvironment

The environment this resource belongs to.

For resources that are created and managed by the CDK
(generally, those created by creating new class instances like Role, Bucket, etc.),
this is always the same as the environment of the stack they belong to;
however, for imported resources
(those obtained from static methods like fromRoleArn, fromBucketName, etc.),
that might be different than the stack they were imported into.

---

##### `stack`<sup>Required</sup> <a name="stack" id="cdk-constructs.ThronEc2Service.property.stack"></a>

```typescript
public readonly stack: Stack;
```

- *Type:* aws-cdk-lib.Stack

The stack in which this resource is defined.

---

##### `cluster`<sup>Required</sup> <a name="cluster" id="cdk-constructs.ThronEc2Service.property.cluster"></a>

```typescript
public readonly cluster: ICluster;
```

- *Type:* aws-cdk-lib.aws_ecs.ICluster

The cluster that hosts the service.

---

##### `connections`<sup>Required</sup> <a name="connections" id="cdk-constructs.ThronEc2Service.property.connections"></a>

```typescript
public readonly connections: Connections;
```

- *Type:* aws-cdk-lib.aws_ec2.Connections

The security groups which manage the allowed network traffic for the service.

---

##### `serviceArn`<sup>Required</sup> <a name="serviceArn" id="cdk-constructs.ThronEc2Service.property.serviceArn"></a>

```typescript
public readonly serviceArn: string;
```

- *Type:* string

The Amazon Resource Name (ARN) of the service.

---

##### `serviceName`<sup>Required</sup> <a name="serviceName" id="cdk-constructs.ThronEc2Service.property.serviceName"></a>

```typescript
public readonly serviceName: string;
```

- *Type:* string

The name of the service.

---

##### `taskDefinition`<sup>Required</sup> <a name="taskDefinition" id="cdk-constructs.ThronEc2Service.property.taskDefinition"></a>

```typescript
public readonly taskDefinition: TaskDefinition;
```

- *Type:* aws-cdk-lib.aws_ecs.TaskDefinition

The task definition to use for tasks in the service.

---

##### `cloudMapService`<sup>Optional</sup> <a name="cloudMapService" id="cdk-constructs.ThronEc2Service.property.cloudMapService"></a>

```typescript
public readonly cloudMapService: IService;
```

- *Type:* aws-cdk-lib.aws_servicediscovery.IService

The CloudMap service created for this service, if any.

---

##### `ec2TaskDefinition`<sup>Required</sup> <a name="ec2TaskDefinition" id="cdk-constructs.ThronEc2Service.property.ec2TaskDefinition"></a>

```typescript
public readonly ec2TaskDefinition: ThronEc2TaskDefinition;
```

- *Type:* <a href="#cdk-constructs.ThronEc2TaskDefinition">ThronEc2TaskDefinition</a>

---

##### `endpoints`<sup>Optional</sup> <a name="endpoints" id="cdk-constructs.ThronEc2Service.property.endpoints"></a>

```typescript
public readonly endpoints: {[ key: string ]: EndpointAlb};
```

- *Type:* {[ key: string ]: <a href="#cdk-constructs.EndpointAlb">EndpointAlb</a>}

---

##### `legacyEndpoints`<sup>Optional</sup> <a name="legacyEndpoints" id="cdk-constructs.ThronEc2Service.property.legacyEndpoints"></a>

```typescript
public readonly legacyEndpoints: {[ key: string ]: EndpointAlb};
```

- *Type:* {[ key: string ]: <a href="#cdk-constructs.EndpointAlb">EndpointAlb</a>}

---

##### `targetScaling`<sup>Optional</sup> <a name="targetScaling" id="cdk-constructs.ThronEc2Service.property.targetScaling"></a>

```typescript
public readonly targetScaling: ThronTargetScaling;
```

- *Type:* <a href="#cdk-constructs.ThronTargetScaling">ThronTargetScaling</a>

---


### ThronEc2TargetScaling <a name="ThronEc2TargetScaling" id="cdk-constructs.ThronEc2TargetScaling"></a>

#### Initializers <a name="Initializers" id="cdk-constructs.ThronEc2TargetScaling.Initializer"></a>

```typescript
import { ThronEc2TargetScaling } from 'cdk-constructs'

new ThronEc2TargetScaling(scope: Construct, id: string, props: ThronEc2TargetScalingProps)
```

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.ThronEc2TargetScaling.Initializer.parameter.scope">scope</a></code> | <code>constructs.Construct</code> | *No description.* |
| <code><a href="#cdk-constructs.ThronEc2TargetScaling.Initializer.parameter.id">id</a></code> | <code>string</code> | *No description.* |
| <code><a href="#cdk-constructs.ThronEc2TargetScaling.Initializer.parameter.props">props</a></code> | <code><a href="#cdk-constructs.ThronEc2TargetScalingProps">ThronEc2TargetScalingProps</a></code> | *No description.* |

---

##### `scope`<sup>Required</sup> <a name="scope" id="cdk-constructs.ThronEc2TargetScaling.Initializer.parameter.scope"></a>

- *Type:* constructs.Construct

---

##### `id`<sup>Required</sup> <a name="id" id="cdk-constructs.ThronEc2TargetScaling.Initializer.parameter.id"></a>

- *Type:* string

---

##### `props`<sup>Required</sup> <a name="props" id="cdk-constructs.ThronEc2TargetScaling.Initializer.parameter.props"></a>

- *Type:* <a href="#cdk-constructs.ThronEc2TargetScalingProps">ThronEc2TargetScalingProps</a>

---

#### Methods <a name="Methods" id="Methods"></a>

| **Name** | **Description** |
| --- | --- |
| <code><a href="#cdk-constructs.ThronEc2TargetScaling.toString">toString</a></code> | Returns a string representation of this construct. |

---

##### `toString` <a name="toString" id="cdk-constructs.ThronEc2TargetScaling.toString"></a>

```typescript
public toString(): string
```

Returns a string representation of this construct.

#### Static Functions <a name="Static Functions" id="Static Functions"></a>

| **Name** | **Description** |
| --- | --- |
| <code><a href="#cdk-constructs.ThronEc2TargetScaling.isConstruct">isConstruct</a></code> | Checks if `x` is a construct. |

---

##### `isConstruct` <a name="isConstruct" id="cdk-constructs.ThronEc2TargetScaling.isConstruct"></a>

```typescript
import { ThronEc2TargetScaling } from 'cdk-constructs'

ThronEc2TargetScaling.isConstruct(x: any)
```

Checks if `x` is a construct.

Use this method instead of `instanceof` to properly detect `Construct`
instances, even when the construct library is symlinked.

Explanation: in JavaScript, multiple copies of the `constructs` library on
disk are seen as independent, completely different libraries. As a
consequence, the class `Construct` in each copy of the `constructs` library
is seen as a different class, and an instance of one class will not test as
`instanceof` the other class. `npm install` will not create installations
like this, but users may manually symlink construct libraries together or
use a monorepo tool: in those cases, multiple copies of the `constructs`
library can be accidentally installed, and `instanceof` will behave
unpredictably. It is safest to avoid using `instanceof`, and using
this type-testing method instead.

###### `x`<sup>Required</sup> <a name="x" id="cdk-constructs.ThronEc2TargetScaling.isConstruct.parameter.x"></a>

- *Type:* any

Any object.

---

#### Properties <a name="Properties" id="Properties"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.ThronEc2TargetScaling.property.node">node</a></code> | <code>constructs.Node</code> | The tree node. |
| <code><a href="#cdk-constructs.ThronEc2TargetScaling.property.maxCapacity">maxCapacity</a></code> | <code>number</code> | The maximum value that Application Auto Scaling can use to scale a target during a scaling activity. |
| <code><a href="#cdk-constructs.ThronEc2TargetScaling.property.minCapacity">minCapacity</a></code> | <code>number</code> | The minimum value that Application Auto Scaling can use to scale a target during a scaling activity. |
| <code><a href="#cdk-constructs.ThronEc2TargetScaling.property.targetValue">targetValue</a></code> | <code>number</code> | The target value for the metric. |
| <code><a href="#cdk-constructs.ThronEc2TargetScaling.property.predefinedMetric">predefinedMetric</a></code> | <code>aws-cdk-lib.aws_applicationautoscaling.PredefinedMetric</code> | A predefined metric for application autoscaling. |
| <code><a href="#cdk-constructs.ThronEc2TargetScaling.property.ec2Service">ec2Service</a></code> | <code>aws-cdk-lib.aws_ecs.Ec2Service</code> | Ec2 Service used as target resource. |
| <code><a href="#cdk-constructs.ThronEc2TargetScaling.property.scalableTarget">scalableTarget</a></code> | <code>aws-cdk-lib.aws_applicationautoscaling.ScalableTarget</code> | *No description.* |
| <code><a href="#cdk-constructs.ThronEc2TargetScaling.property.targetTrackingScalingPolicy">targetTrackingScalingPolicy</a></code> | <code>aws-cdk-lib.aws_applicationautoscaling.TargetTrackingScalingPolicy</code> | *No description.* |

---

##### `node`<sup>Required</sup> <a name="node" id="cdk-constructs.ThronEc2TargetScaling.property.node"></a>

```typescript
public readonly node: Node;
```

- *Type:* constructs.Node

The tree node.

---

##### `maxCapacity`<sup>Required</sup> <a name="maxCapacity" id="cdk-constructs.ThronEc2TargetScaling.property.maxCapacity"></a>

```typescript
public readonly maxCapacity: number;
```

- *Type:* number

The maximum value that Application Auto Scaling can use to scale a target during a scaling activity.

---

##### `minCapacity`<sup>Required</sup> <a name="minCapacity" id="cdk-constructs.ThronEc2TargetScaling.property.minCapacity"></a>

```typescript
public readonly minCapacity: number;
```

- *Type:* number

The minimum value that Application Auto Scaling can use to scale a target during a scaling activity.

---

##### `targetValue`<sup>Required</sup> <a name="targetValue" id="cdk-constructs.ThronEc2TargetScaling.property.targetValue"></a>

```typescript
public readonly targetValue: number;
```

- *Type:* number

The target value for the metric.

---

##### `predefinedMetric`<sup>Optional</sup> <a name="predefinedMetric" id="cdk-constructs.ThronEc2TargetScaling.property.predefinedMetric"></a>

```typescript
public readonly predefinedMetric: PredefinedMetric;
```

- *Type:* aws-cdk-lib.aws_applicationautoscaling.PredefinedMetric

A predefined metric for application autoscaling.

The metric must track utilization. Scaling out will happen if the metric is higher than the target value,
scaling in will happen in the metric is lower than the target value.

---

##### `ec2Service`<sup>Required</sup> <a name="ec2Service" id="cdk-constructs.ThronEc2TargetScaling.property.ec2Service"></a>

```typescript
public readonly ec2Service: Ec2Service;
```

- *Type:* aws-cdk-lib.aws_ecs.Ec2Service

Ec2 Service used as target resource.

---

##### `scalableTarget`<sup>Required</sup> <a name="scalableTarget" id="cdk-constructs.ThronEc2TargetScaling.property.scalableTarget"></a>

```typescript
public readonly scalableTarget: ScalableTarget;
```

- *Type:* aws-cdk-lib.aws_applicationautoscaling.ScalableTarget

---

##### `targetTrackingScalingPolicy`<sup>Required</sup> <a name="targetTrackingScalingPolicy" id="cdk-constructs.ThronEc2TargetScaling.property.targetTrackingScalingPolicy"></a>

```typescript
public readonly targetTrackingScalingPolicy: TargetTrackingScalingPolicy;
```

- *Type:* aws-cdk-lib.aws_applicationautoscaling.TargetTrackingScalingPolicy

---


### ThronEc2TaskDefinition <a name="ThronEc2TaskDefinition" id="cdk-constructs.ThronEc2TaskDefinition"></a>

#### Initializers <a name="Initializers" id="cdk-constructs.ThronEc2TaskDefinition.Initializer"></a>

```typescript
import { ThronEc2TaskDefinition } from 'cdk-constructs'

new ThronEc2TaskDefinition(scope: Stack, id: string, props: ThronEc2TaskDefinitionProps)
```

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.ThronEc2TaskDefinition.Initializer.parameter.scope">scope</a></code> | <code>aws-cdk-lib.Stack</code> | *No description.* |
| <code><a href="#cdk-constructs.ThronEc2TaskDefinition.Initializer.parameter.id">id</a></code> | <code>string</code> | *No description.* |
| <code><a href="#cdk-constructs.ThronEc2TaskDefinition.Initializer.parameter.props">props</a></code> | <code><a href="#cdk-constructs.ThronEc2TaskDefinitionProps">ThronEc2TaskDefinitionProps</a></code> | *No description.* |

---

##### `scope`<sup>Required</sup> <a name="scope" id="cdk-constructs.ThronEc2TaskDefinition.Initializer.parameter.scope"></a>

- *Type:* aws-cdk-lib.Stack

---

##### `id`<sup>Required</sup> <a name="id" id="cdk-constructs.ThronEc2TaskDefinition.Initializer.parameter.id"></a>

- *Type:* string

---

##### `props`<sup>Required</sup> <a name="props" id="cdk-constructs.ThronEc2TaskDefinition.Initializer.parameter.props"></a>

- *Type:* <a href="#cdk-constructs.ThronEc2TaskDefinitionProps">ThronEc2TaskDefinitionProps</a>

---

#### Methods <a name="Methods" id="Methods"></a>

| **Name** | **Description** |
| --- | --- |
| <code><a href="#cdk-constructs.ThronEc2TaskDefinition.toString">toString</a></code> | Returns a string representation of this construct. |
| <code><a href="#cdk-constructs.ThronEc2TaskDefinition.applyRemovalPolicy">applyRemovalPolicy</a></code> | Apply the given removal policy to this resource. |
| <code><a href="#cdk-constructs.ThronEc2TaskDefinition.addContainer">addContainer</a></code> | Tasks running in AWSVPC networking mode requires an additional environment variable for the region to be sourced. |
| <code><a href="#cdk-constructs.ThronEc2TaskDefinition.addExtension">addExtension</a></code> | Adds the specified extension to the task definition. |
| <code><a href="#cdk-constructs.ThronEc2TaskDefinition.addFirelensLogRouter">addFirelensLogRouter</a></code> | Adds a firelens log router to the task definition. |
| <code><a href="#cdk-constructs.ThronEc2TaskDefinition.addInferenceAccelerator">addInferenceAccelerator</a></code> | Adds an inference accelerator to the task definition. |
| <code><a href="#cdk-constructs.ThronEc2TaskDefinition.addPlacementConstraint">addPlacementConstraint</a></code> | Adds the specified placement constraint to the task definition. |
| <code><a href="#cdk-constructs.ThronEc2TaskDefinition.addToExecutionRolePolicy">addToExecutionRolePolicy</a></code> | Adds a policy statement to the task execution IAM role. |
| <code><a href="#cdk-constructs.ThronEc2TaskDefinition.addToTaskRolePolicy">addToTaskRolePolicy</a></code> | Adds a policy statement to the task IAM role. |
| <code><a href="#cdk-constructs.ThronEc2TaskDefinition.addVolume">addVolume</a></code> | Adds a volume to the task definition. |
| <code><a href="#cdk-constructs.ThronEc2TaskDefinition.findContainer">findContainer</a></code> | Returns the container that match the provided containerName. |
| <code><a href="#cdk-constructs.ThronEc2TaskDefinition.findPortMappingByName">findPortMappingByName</a></code> | Determine the existing port mapping for the provided name. |
| <code><a href="#cdk-constructs.ThronEc2TaskDefinition.grantRun">grantRun</a></code> | Grants permissions to run this task definition. |
| <code><a href="#cdk-constructs.ThronEc2TaskDefinition.obtainExecutionRole">obtainExecutionRole</a></code> | Creates the task execution IAM role if it doesn't already exist. |

---

##### `toString` <a name="toString" id="cdk-constructs.ThronEc2TaskDefinition.toString"></a>

```typescript
public toString(): string
```

Returns a string representation of this construct.

##### `applyRemovalPolicy` <a name="applyRemovalPolicy" id="cdk-constructs.ThronEc2TaskDefinition.applyRemovalPolicy"></a>

```typescript
public applyRemovalPolicy(policy: RemovalPolicy): void
```

Apply the given removal policy to this resource.

The Removal Policy controls what happens to this resource when it stops
being managed by CloudFormation, either because you've removed it from the
CDK application or because you've made a change that requires the resource
to be replaced.

The resource can be deleted (`RemovalPolicy.DESTROY`), or left in your AWS
account for data recovery and cleanup later (`RemovalPolicy.RETAIN`).

###### `policy`<sup>Required</sup> <a name="policy" id="cdk-constructs.ThronEc2TaskDefinition.applyRemovalPolicy.parameter.policy"></a>

- *Type:* aws-cdk-lib.RemovalPolicy

---

##### `addContainer` <a name="addContainer" id="cdk-constructs.ThronEc2TaskDefinition.addContainer"></a>

```typescript
public addContainer(id: string, props: ContainerDefinitionOptions): ContainerDefinition
```

Tasks running in AWSVPC networking mode requires an additional environment variable for the region to be sourced.

This override adds in the additional environment variable as required

###### `id`<sup>Required</sup> <a name="id" id="cdk-constructs.ThronEc2TaskDefinition.addContainer.parameter.id"></a>

- *Type:* string

---

###### `props`<sup>Required</sup> <a name="props" id="cdk-constructs.ThronEc2TaskDefinition.addContainer.parameter.props"></a>

- *Type:* aws-cdk-lib.aws_ecs.ContainerDefinitionOptions

---

##### `addExtension` <a name="addExtension" id="cdk-constructs.ThronEc2TaskDefinition.addExtension"></a>

```typescript
public addExtension(extension: ITaskDefinitionExtension): void
```

Adds the specified extension to the task definition.

Extension can be used to apply a packaged modification to
a task definition.

###### `extension`<sup>Required</sup> <a name="extension" id="cdk-constructs.ThronEc2TaskDefinition.addExtension.parameter.extension"></a>

- *Type:* aws-cdk-lib.aws_ecs.ITaskDefinitionExtension

---

##### `addFirelensLogRouter` <a name="addFirelensLogRouter" id="cdk-constructs.ThronEc2TaskDefinition.addFirelensLogRouter"></a>

```typescript
public addFirelensLogRouter(id: string, props: FirelensLogRouterDefinitionOptions): FirelensLogRouter
```

Adds a firelens log router to the task definition.

###### `id`<sup>Required</sup> <a name="id" id="cdk-constructs.ThronEc2TaskDefinition.addFirelensLogRouter.parameter.id"></a>

- *Type:* string

---

###### `props`<sup>Required</sup> <a name="props" id="cdk-constructs.ThronEc2TaskDefinition.addFirelensLogRouter.parameter.props"></a>

- *Type:* aws-cdk-lib.aws_ecs.FirelensLogRouterDefinitionOptions

---

##### ~~`addInferenceAccelerator`~~ <a name="addInferenceAccelerator" id="cdk-constructs.ThronEc2TaskDefinition.addInferenceAccelerator"></a>

```typescript
public addInferenceAccelerator(inferenceAccelerator: InferenceAccelerator): void
```

Adds an inference accelerator to the task definition.

###### `inferenceAccelerator`<sup>Required</sup> <a name="inferenceAccelerator" id="cdk-constructs.ThronEc2TaskDefinition.addInferenceAccelerator.parameter.inferenceAccelerator"></a>

- *Type:* aws-cdk-lib.aws_ecs.InferenceAccelerator

---

##### `addPlacementConstraint` <a name="addPlacementConstraint" id="cdk-constructs.ThronEc2TaskDefinition.addPlacementConstraint"></a>

```typescript
public addPlacementConstraint(constraint: PlacementConstraint): void
```

Adds the specified placement constraint to the task definition.

###### `constraint`<sup>Required</sup> <a name="constraint" id="cdk-constructs.ThronEc2TaskDefinition.addPlacementConstraint.parameter.constraint"></a>

- *Type:* aws-cdk-lib.aws_ecs.PlacementConstraint

---

##### `addToExecutionRolePolicy` <a name="addToExecutionRolePolicy" id="cdk-constructs.ThronEc2TaskDefinition.addToExecutionRolePolicy"></a>

```typescript
public addToExecutionRolePolicy(statement: PolicyStatement): void
```

Adds a policy statement to the task execution IAM role.

###### `statement`<sup>Required</sup> <a name="statement" id="cdk-constructs.ThronEc2TaskDefinition.addToExecutionRolePolicy.parameter.statement"></a>

- *Type:* aws-cdk-lib.aws_iam.PolicyStatement

---

##### `addToTaskRolePolicy` <a name="addToTaskRolePolicy" id="cdk-constructs.ThronEc2TaskDefinition.addToTaskRolePolicy"></a>

```typescript
public addToTaskRolePolicy(statement: PolicyStatement): void
```

Adds a policy statement to the task IAM role.

###### `statement`<sup>Required</sup> <a name="statement" id="cdk-constructs.ThronEc2TaskDefinition.addToTaskRolePolicy.parameter.statement"></a>

- *Type:* aws-cdk-lib.aws_iam.PolicyStatement

---

##### `addVolume` <a name="addVolume" id="cdk-constructs.ThronEc2TaskDefinition.addVolume"></a>

```typescript
public addVolume(volume: Volume): void
```

Adds a volume to the task definition.

###### `volume`<sup>Required</sup> <a name="volume" id="cdk-constructs.ThronEc2TaskDefinition.addVolume.parameter.volume"></a>

- *Type:* aws-cdk-lib.aws_ecs.Volume

---

##### `findContainer` <a name="findContainer" id="cdk-constructs.ThronEc2TaskDefinition.findContainer"></a>

```typescript
public findContainer(containerName: string): ContainerDefinition
```

Returns the container that match the provided containerName.

###### `containerName`<sup>Required</sup> <a name="containerName" id="cdk-constructs.ThronEc2TaskDefinition.findContainer.parameter.containerName"></a>

- *Type:* string

---

##### `findPortMappingByName` <a name="findPortMappingByName" id="cdk-constructs.ThronEc2TaskDefinition.findPortMappingByName"></a>

```typescript
public findPortMappingByName(name: string): PortMapping
```

Determine the existing port mapping for the provided name.

###### `name`<sup>Required</sup> <a name="name" id="cdk-constructs.ThronEc2TaskDefinition.findPortMappingByName.parameter.name"></a>

- *Type:* string

: port mapping name.

---

##### `grantRun` <a name="grantRun" id="cdk-constructs.ThronEc2TaskDefinition.grantRun"></a>

```typescript
public grantRun(grantee: IGrantable): Grant
```

Grants permissions to run this task definition.

This will grant the following permissions:

  - ecs:RunTask
  - iam:PassRole

###### `grantee`<sup>Required</sup> <a name="grantee" id="cdk-constructs.ThronEc2TaskDefinition.grantRun.parameter.grantee"></a>

- *Type:* aws-cdk-lib.aws_iam.IGrantable

Principal to grant consume rights to.

---

##### `obtainExecutionRole` <a name="obtainExecutionRole" id="cdk-constructs.ThronEc2TaskDefinition.obtainExecutionRole"></a>

```typescript
public obtainExecutionRole(): IRole
```

Creates the task execution IAM role if it doesn't already exist.

#### Static Functions <a name="Static Functions" id="Static Functions"></a>

| **Name** | **Description** |
| --- | --- |
| <code><a href="#cdk-constructs.ThronEc2TaskDefinition.isConstruct">isConstruct</a></code> | Checks if `x` is a construct. |
| <code><a href="#cdk-constructs.ThronEc2TaskDefinition.isOwnedResource">isOwnedResource</a></code> | Returns true if the construct was created by CDK, and false otherwise. |
| <code><a href="#cdk-constructs.ThronEc2TaskDefinition.isResource">isResource</a></code> | Check whether the given construct is a Resource. |
| <code><a href="#cdk-constructs.ThronEc2TaskDefinition.fromTaskDefinitionArn">fromTaskDefinitionArn</a></code> | Imports a task definition from the specified task definition ARN. |
| <code><a href="#cdk-constructs.ThronEc2TaskDefinition.fromTaskDefinitionAttributes">fromTaskDefinitionAttributes</a></code> | Create a task definition from a task definition reference. |
| <code><a href="#cdk-constructs.ThronEc2TaskDefinition.fromEc2TaskDefinitionArn">fromEc2TaskDefinitionArn</a></code> | Imports a task definition from the specified task definition ARN. |
| <code><a href="#cdk-constructs.ThronEc2TaskDefinition.fromEc2TaskDefinitionAttributes">fromEc2TaskDefinitionAttributes</a></code> | Imports an existing Ec2 task definition from its attributes. |

---

##### `isConstruct` <a name="isConstruct" id="cdk-constructs.ThronEc2TaskDefinition.isConstruct"></a>

```typescript
import { ThronEc2TaskDefinition } from 'cdk-constructs'

ThronEc2TaskDefinition.isConstruct(x: any)
```

Checks if `x` is a construct.

Use this method instead of `instanceof` to properly detect `Construct`
instances, even when the construct library is symlinked.

Explanation: in JavaScript, multiple copies of the `constructs` library on
disk are seen as independent, completely different libraries. As a
consequence, the class `Construct` in each copy of the `constructs` library
is seen as a different class, and an instance of one class will not test as
`instanceof` the other class. `npm install` will not create installations
like this, but users may manually symlink construct libraries together or
use a monorepo tool: in those cases, multiple copies of the `constructs`
library can be accidentally installed, and `instanceof` will behave
unpredictably. It is safest to avoid using `instanceof`, and using
this type-testing method instead.

###### `x`<sup>Required</sup> <a name="x" id="cdk-constructs.ThronEc2TaskDefinition.isConstruct.parameter.x"></a>

- *Type:* any

Any object.

---

##### `isOwnedResource` <a name="isOwnedResource" id="cdk-constructs.ThronEc2TaskDefinition.isOwnedResource"></a>

```typescript
import { ThronEc2TaskDefinition } from 'cdk-constructs'

ThronEc2TaskDefinition.isOwnedResource(construct: IConstruct)
```

Returns true if the construct was created by CDK, and false otherwise.

###### `construct`<sup>Required</sup> <a name="construct" id="cdk-constructs.ThronEc2TaskDefinition.isOwnedResource.parameter.construct"></a>

- *Type:* constructs.IConstruct

---

##### `isResource` <a name="isResource" id="cdk-constructs.ThronEc2TaskDefinition.isResource"></a>

```typescript
import { ThronEc2TaskDefinition } from 'cdk-constructs'

ThronEc2TaskDefinition.isResource(construct: IConstruct)
```

Check whether the given construct is a Resource.

###### `construct`<sup>Required</sup> <a name="construct" id="cdk-constructs.ThronEc2TaskDefinition.isResource.parameter.construct"></a>

- *Type:* constructs.IConstruct

---

##### `fromTaskDefinitionArn` <a name="fromTaskDefinitionArn" id="cdk-constructs.ThronEc2TaskDefinition.fromTaskDefinitionArn"></a>

```typescript
import { ThronEc2TaskDefinition } from 'cdk-constructs'

ThronEc2TaskDefinition.fromTaskDefinitionArn(scope: Construct, id: string, taskDefinitionArn: string)
```

Imports a task definition from the specified task definition ARN.

The task will have a compatibility of EC2+Fargate.

###### `scope`<sup>Required</sup> <a name="scope" id="cdk-constructs.ThronEc2TaskDefinition.fromTaskDefinitionArn.parameter.scope"></a>

- *Type:* constructs.Construct

---

###### `id`<sup>Required</sup> <a name="id" id="cdk-constructs.ThronEc2TaskDefinition.fromTaskDefinitionArn.parameter.id"></a>

- *Type:* string

---

###### `taskDefinitionArn`<sup>Required</sup> <a name="taskDefinitionArn" id="cdk-constructs.ThronEc2TaskDefinition.fromTaskDefinitionArn.parameter.taskDefinitionArn"></a>

- *Type:* string

---

##### `fromTaskDefinitionAttributes` <a name="fromTaskDefinitionAttributes" id="cdk-constructs.ThronEc2TaskDefinition.fromTaskDefinitionAttributes"></a>

```typescript
import { ThronEc2TaskDefinition } from 'cdk-constructs'

ThronEc2TaskDefinition.fromTaskDefinitionAttributes(scope: Construct, id: string, attrs: TaskDefinitionAttributes)
```

Create a task definition from a task definition reference.

###### `scope`<sup>Required</sup> <a name="scope" id="cdk-constructs.ThronEc2TaskDefinition.fromTaskDefinitionAttributes.parameter.scope"></a>

- *Type:* constructs.Construct

---

###### `id`<sup>Required</sup> <a name="id" id="cdk-constructs.ThronEc2TaskDefinition.fromTaskDefinitionAttributes.parameter.id"></a>

- *Type:* string

---

###### `attrs`<sup>Required</sup> <a name="attrs" id="cdk-constructs.ThronEc2TaskDefinition.fromTaskDefinitionAttributes.parameter.attrs"></a>

- *Type:* aws-cdk-lib.aws_ecs.TaskDefinitionAttributes

---

##### `fromEc2TaskDefinitionArn` <a name="fromEc2TaskDefinitionArn" id="cdk-constructs.ThronEc2TaskDefinition.fromEc2TaskDefinitionArn"></a>

```typescript
import { ThronEc2TaskDefinition } from 'cdk-constructs'

ThronEc2TaskDefinition.fromEc2TaskDefinitionArn(scope: Construct, id: string, ec2TaskDefinitionArn: string)
```

Imports a task definition from the specified task definition ARN.

###### `scope`<sup>Required</sup> <a name="scope" id="cdk-constructs.ThronEc2TaskDefinition.fromEc2TaskDefinitionArn.parameter.scope"></a>

- *Type:* constructs.Construct

---

###### `id`<sup>Required</sup> <a name="id" id="cdk-constructs.ThronEc2TaskDefinition.fromEc2TaskDefinitionArn.parameter.id"></a>

- *Type:* string

---

###### `ec2TaskDefinitionArn`<sup>Required</sup> <a name="ec2TaskDefinitionArn" id="cdk-constructs.ThronEc2TaskDefinition.fromEc2TaskDefinitionArn.parameter.ec2TaskDefinitionArn"></a>

- *Type:* string

---

##### `fromEc2TaskDefinitionAttributes` <a name="fromEc2TaskDefinitionAttributes" id="cdk-constructs.ThronEc2TaskDefinition.fromEc2TaskDefinitionAttributes"></a>

```typescript
import { ThronEc2TaskDefinition } from 'cdk-constructs'

ThronEc2TaskDefinition.fromEc2TaskDefinitionAttributes(scope: Construct, id: string, attrs: Ec2TaskDefinitionAttributes)
```

Imports an existing Ec2 task definition from its attributes.

###### `scope`<sup>Required</sup> <a name="scope" id="cdk-constructs.ThronEc2TaskDefinition.fromEc2TaskDefinitionAttributes.parameter.scope"></a>

- *Type:* constructs.Construct

---

###### `id`<sup>Required</sup> <a name="id" id="cdk-constructs.ThronEc2TaskDefinition.fromEc2TaskDefinitionAttributes.parameter.id"></a>

- *Type:* string

---

###### `attrs`<sup>Required</sup> <a name="attrs" id="cdk-constructs.ThronEc2TaskDefinition.fromEc2TaskDefinitionAttributes.parameter.attrs"></a>

- *Type:* aws-cdk-lib.aws_ecs.Ec2TaskDefinitionAttributes

---

#### Properties <a name="Properties" id="Properties"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.ThronEc2TaskDefinition.property.node">node</a></code> | <code>constructs.Node</code> | The tree node. |
| <code><a href="#cdk-constructs.ThronEc2TaskDefinition.property.env">env</a></code> | <code>aws-cdk-lib.ResourceEnvironment</code> | The environment this resource belongs to. |
| <code><a href="#cdk-constructs.ThronEc2TaskDefinition.property.stack">stack</a></code> | <code>aws-cdk-lib.Stack</code> | The stack in which this resource is defined. |
| <code><a href="#cdk-constructs.ThronEc2TaskDefinition.property.compatibility">compatibility</a></code> | <code>aws-cdk-lib.aws_ecs.Compatibility</code> | The task launch type compatibility requirement. |
| <code><a href="#cdk-constructs.ThronEc2TaskDefinition.property.family">family</a></code> | <code>string</code> | The name of a family that this task definition is registered to. |
| <code><a href="#cdk-constructs.ThronEc2TaskDefinition.property.inferenceAccelerators">inferenceAccelerators</a></code> | <code>aws-cdk-lib.aws_ecs.InferenceAccelerator[]</code> | Public getter method to access list of inference accelerators attached to the instance. |
| <code><a href="#cdk-constructs.ThronEc2TaskDefinition.property.isEc2Compatible">isEc2Compatible</a></code> | <code>boolean</code> | Return true if the task definition can be run on an EC2 cluster. |
| <code><a href="#cdk-constructs.ThronEc2TaskDefinition.property.isExternalCompatible">isExternalCompatible</a></code> | <code>boolean</code> | Return true if the task definition can be run on a ECS anywhere cluster. |
| <code><a href="#cdk-constructs.ThronEc2TaskDefinition.property.isFargateCompatible">isFargateCompatible</a></code> | <code>boolean</code> | Return true if the task definition can be run on a Fargate cluster. |
| <code><a href="#cdk-constructs.ThronEc2TaskDefinition.property.networkMode">networkMode</a></code> | <code>aws-cdk-lib.aws_ecs.NetworkMode</code> | The networking mode to use for the containers in the task. |
| <code><a href="#cdk-constructs.ThronEc2TaskDefinition.property.taskDefinitionArn">taskDefinitionArn</a></code> | <code>string</code> | The full Amazon Resource Name (ARN) of the task definition. |
| <code><a href="#cdk-constructs.ThronEc2TaskDefinition.property.taskRole">taskRole</a></code> | <code>aws-cdk-lib.aws_iam.IRole</code> | The name of the IAM role that grants containers in the task permission to call AWS APIs on your behalf. |
| <code><a href="#cdk-constructs.ThronEc2TaskDefinition.property.ephemeralStorageGiB">ephemeralStorageGiB</a></code> | <code>number</code> | The amount (in GiB) of ephemeral storage to be allocated to the task. |
| <code><a href="#cdk-constructs.ThronEc2TaskDefinition.property.executionRole">executionRole</a></code> | <code>aws-cdk-lib.aws_iam.IRole</code> | Execution role for this task definition. |
| <code><a href="#cdk-constructs.ThronEc2TaskDefinition.property.pidMode">pidMode</a></code> | <code>aws-cdk-lib.aws_ecs.PidMode</code> | The process namespace to use for the containers in the task. |
| <code><a href="#cdk-constructs.ThronEc2TaskDefinition.property.referencesSecretJsonField">referencesSecretJsonField</a></code> | <code>boolean</code> | Whether this task definition has at least a container that references a specific JSON field of a secret stored in Secrets Manager. |
| <code><a href="#cdk-constructs.ThronEc2TaskDefinition.property.defaultContainer">defaultContainer</a></code> | <code>aws-cdk-lib.aws_ecs.ContainerDefinition</code> | Default container for this task. |
| <code><a href="#cdk-constructs.ThronEc2TaskDefinition.property.container">container</a></code> | <code>aws-cdk-lib.aws_ecs.ContainerDefinition</code> | *No description.* |
| <code><a href="#cdk-constructs.ThronEc2TaskDefinition.property.logs">logs</a></code> | <code>aws-cdk-lib.aws_logs.LogGroup</code> | *No description.* |
| <code><a href="#cdk-constructs.ThronEc2TaskDefinition.property.port">port</a></code> | <code>number</code> | The port exposed for connection. |
| <code><a href="#cdk-constructs.ThronEc2TaskDefinition.property.prometheusMetricsPath">prometheusMetricsPath</a></code> | <code>string</code> | *No description.* |

---

##### `node`<sup>Required</sup> <a name="node" id="cdk-constructs.ThronEc2TaskDefinition.property.node"></a>

```typescript
public readonly node: Node;
```

- *Type:* constructs.Node

The tree node.

---

##### `env`<sup>Required</sup> <a name="env" id="cdk-constructs.ThronEc2TaskDefinition.property.env"></a>

```typescript
public readonly env: ResourceEnvironment;
```

- *Type:* aws-cdk-lib.ResourceEnvironment

The environment this resource belongs to.

For resources that are created and managed by the CDK
(generally, those created by creating new class instances like Role, Bucket, etc.),
this is always the same as the environment of the stack they belong to;
however, for imported resources
(those obtained from static methods like fromRoleArn, fromBucketName, etc.),
that might be different than the stack they were imported into.

---

##### `stack`<sup>Required</sup> <a name="stack" id="cdk-constructs.ThronEc2TaskDefinition.property.stack"></a>

```typescript
public readonly stack: Stack;
```

- *Type:* aws-cdk-lib.Stack

The stack in which this resource is defined.

---

##### `compatibility`<sup>Required</sup> <a name="compatibility" id="cdk-constructs.ThronEc2TaskDefinition.property.compatibility"></a>

```typescript
public readonly compatibility: Compatibility;
```

- *Type:* aws-cdk-lib.aws_ecs.Compatibility

The task launch type compatibility requirement.

---

##### `family`<sup>Required</sup> <a name="family" id="cdk-constructs.ThronEc2TaskDefinition.property.family"></a>

```typescript
public readonly family: string;
```

- *Type:* string

The name of a family that this task definition is registered to.

A family groups multiple versions of a task definition.

---

##### `inferenceAccelerators`<sup>Required</sup> <a name="inferenceAccelerators" id="cdk-constructs.ThronEc2TaskDefinition.property.inferenceAccelerators"></a>

```typescript
public readonly inferenceAccelerators: InferenceAccelerator[];
```

- *Type:* aws-cdk-lib.aws_ecs.InferenceAccelerator[]

Public getter method to access list of inference accelerators attached to the instance.

---

##### `isEc2Compatible`<sup>Required</sup> <a name="isEc2Compatible" id="cdk-constructs.ThronEc2TaskDefinition.property.isEc2Compatible"></a>

```typescript
public readonly isEc2Compatible: boolean;
```

- *Type:* boolean

Return true if the task definition can be run on an EC2 cluster.

---

##### `isExternalCompatible`<sup>Required</sup> <a name="isExternalCompatible" id="cdk-constructs.ThronEc2TaskDefinition.property.isExternalCompatible"></a>

```typescript
public readonly isExternalCompatible: boolean;
```

- *Type:* boolean

Return true if the task definition can be run on a ECS anywhere cluster.

---

##### `isFargateCompatible`<sup>Required</sup> <a name="isFargateCompatible" id="cdk-constructs.ThronEc2TaskDefinition.property.isFargateCompatible"></a>

```typescript
public readonly isFargateCompatible: boolean;
```

- *Type:* boolean

Return true if the task definition can be run on a Fargate cluster.

---

##### `networkMode`<sup>Required</sup> <a name="networkMode" id="cdk-constructs.ThronEc2TaskDefinition.property.networkMode"></a>

```typescript
public readonly networkMode: NetworkMode;
```

- *Type:* aws-cdk-lib.aws_ecs.NetworkMode

The networking mode to use for the containers in the task.

---

##### `taskDefinitionArn`<sup>Required</sup> <a name="taskDefinitionArn" id="cdk-constructs.ThronEc2TaskDefinition.property.taskDefinitionArn"></a>

```typescript
public readonly taskDefinitionArn: string;
```

- *Type:* string

The full Amazon Resource Name (ARN) of the task definition.

---

##### `taskRole`<sup>Required</sup> <a name="taskRole" id="cdk-constructs.ThronEc2TaskDefinition.property.taskRole"></a>

```typescript
public readonly taskRole: IRole;
```

- *Type:* aws-cdk-lib.aws_iam.IRole

The name of the IAM role that grants containers in the task permission to call AWS APIs on your behalf.

---

##### `ephemeralStorageGiB`<sup>Optional</sup> <a name="ephemeralStorageGiB" id="cdk-constructs.ThronEc2TaskDefinition.property.ephemeralStorageGiB"></a>

```typescript
public readonly ephemeralStorageGiB: number;
```

- *Type:* number

The amount (in GiB) of ephemeral storage to be allocated to the task.

Only supported in Fargate platform version 1.4.0 or later.

---

##### `executionRole`<sup>Optional</sup> <a name="executionRole" id="cdk-constructs.ThronEc2TaskDefinition.property.executionRole"></a>

```typescript
public readonly executionRole: IRole;
```

- *Type:* aws-cdk-lib.aws_iam.IRole

Execution role for this task definition.

---

##### `pidMode`<sup>Optional</sup> <a name="pidMode" id="cdk-constructs.ThronEc2TaskDefinition.property.pidMode"></a>

```typescript
public readonly pidMode: PidMode;
```

- *Type:* aws-cdk-lib.aws_ecs.PidMode

The process namespace to use for the containers in the task.

Only supported for tasks that are hosted on AWS Fargate if the tasks
are using platform version 1.4.0 or later (Linux). Not supported in
Windows containers. If pidMode is specified for a Fargate task,
then runtimePlatform.operatingSystemFamily must also be specified.  For more
information, see [Task Definition Parameters](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/task_definition_parameters.html#task_definition_pidmode).

---

##### `referencesSecretJsonField`<sup>Optional</sup> <a name="referencesSecretJsonField" id="cdk-constructs.ThronEc2TaskDefinition.property.referencesSecretJsonField"></a>

```typescript
public readonly referencesSecretJsonField: boolean;
```

- *Type:* boolean

Whether this task definition has at least a container that references a specific JSON field of a secret stored in Secrets Manager.

---

##### `defaultContainer`<sup>Optional</sup> <a name="defaultContainer" id="cdk-constructs.ThronEc2TaskDefinition.property.defaultContainer"></a>

```typescript
public readonly defaultContainer: ContainerDefinition;
```

- *Type:* aws-cdk-lib.aws_ecs.ContainerDefinition

Default container for this task.

Load balancers will send traffic to this container. The first
essential container that is added to this task will become the default
container.

---

##### `container`<sup>Required</sup> <a name="container" id="cdk-constructs.ThronEc2TaskDefinition.property.container"></a>

```typescript
public readonly container: ContainerDefinition;
```

- *Type:* aws-cdk-lib.aws_ecs.ContainerDefinition

---

##### `logs`<sup>Required</sup> <a name="logs" id="cdk-constructs.ThronEc2TaskDefinition.property.logs"></a>

```typescript
public readonly logs: LogGroup;
```

- *Type:* aws-cdk-lib.aws_logs.LogGroup

---

##### `port`<sup>Optional</sup> <a name="port" id="cdk-constructs.ThronEc2TaskDefinition.property.port"></a>

```typescript
public readonly port: number;
```

- *Type:* number

The port exposed for connection.

---

##### `prometheusMetricsPath`<sup>Optional</sup> <a name="prometheusMetricsPath" id="cdk-constructs.ThronEc2TaskDefinition.property.prometheusMetricsPath"></a>

```typescript
public readonly prometheusMetricsPath: string;
```

- *Type:* string

---


### ThronEndpointApiGateway <a name="ThronEndpointApiGateway" id="cdk-constructs.ThronEndpointApiGateway"></a>

This constructs creates an API Gateway Endpoint for a Lambda Function.

It takes care
of creating also its domain following THRON's convention.

#### Initializers <a name="Initializers" id="cdk-constructs.ThronEndpointApiGateway.Initializer"></a>

```typescript
import { ThronEndpointApiGateway } from 'cdk-constructs'

new ThronEndpointApiGateway(scope: Construct, id: string, props: ThronEndpointApiGatewayProps)
```

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.ThronEndpointApiGateway.Initializer.parameter.scope">scope</a></code> | <code>constructs.Construct</code> | *No description.* |
| <code><a href="#cdk-constructs.ThronEndpointApiGateway.Initializer.parameter.id">id</a></code> | <code>string</code> | *No description.* |
| <code><a href="#cdk-constructs.ThronEndpointApiGateway.Initializer.parameter.props">props</a></code> | <code><a href="#cdk-constructs.ThronEndpointApiGatewayProps">ThronEndpointApiGatewayProps</a></code> | *No description.* |

---

##### `scope`<sup>Required</sup> <a name="scope" id="cdk-constructs.ThronEndpointApiGateway.Initializer.parameter.scope"></a>

- *Type:* constructs.Construct

---

##### `id`<sup>Required</sup> <a name="id" id="cdk-constructs.ThronEndpointApiGateway.Initializer.parameter.id"></a>

- *Type:* string

---

##### `props`<sup>Required</sup> <a name="props" id="cdk-constructs.ThronEndpointApiGateway.Initializer.parameter.props"></a>

- *Type:* <a href="#cdk-constructs.ThronEndpointApiGatewayProps">ThronEndpointApiGatewayProps</a>

---

#### Methods <a name="Methods" id="Methods"></a>

| **Name** | **Description** |
| --- | --- |
| <code><a href="#cdk-constructs.ThronEndpointApiGateway.toString">toString</a></code> | Returns a string representation of this construct. |

---

##### `toString` <a name="toString" id="cdk-constructs.ThronEndpointApiGateway.toString"></a>

```typescript
public toString(): string
```

Returns a string representation of this construct.

#### Static Functions <a name="Static Functions" id="Static Functions"></a>

| **Name** | **Description** |
| --- | --- |
| <code><a href="#cdk-constructs.ThronEndpointApiGateway.isConstruct">isConstruct</a></code> | Checks if `x` is a construct. |

---

##### `isConstruct` <a name="isConstruct" id="cdk-constructs.ThronEndpointApiGateway.isConstruct"></a>

```typescript
import { ThronEndpointApiGateway } from 'cdk-constructs'

ThronEndpointApiGateway.isConstruct(x: any)
```

Checks if `x` is a construct.

Use this method instead of `instanceof` to properly detect `Construct`
instances, even when the construct library is symlinked.

Explanation: in JavaScript, multiple copies of the `constructs` library on
disk are seen as independent, completely different libraries. As a
consequence, the class `Construct` in each copy of the `constructs` library
is seen as a different class, and an instance of one class will not test as
`instanceof` the other class. `npm install` will not create installations
like this, but users may manually symlink construct libraries together or
use a monorepo tool: in those cases, multiple copies of the `constructs`
library can be accidentally installed, and `instanceof` will behave
unpredictably. It is safest to avoid using `instanceof`, and using
this type-testing method instead.

###### `x`<sup>Required</sup> <a name="x" id="cdk-constructs.ThronEndpointApiGateway.isConstruct.parameter.x"></a>

- *Type:* any

Any object.

---

#### Properties <a name="Properties" id="Properties"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.ThronEndpointApiGateway.property.node">node</a></code> | <code>constructs.Node</code> | The tree node. |

---

##### `node`<sup>Required</sup> <a name="node" id="cdk-constructs.ThronEndpointApiGateway.property.node"></a>

```typescript
public readonly node: Node;
```

- *Type:* constructs.Node

The tree node.

---


### ThronLambdaMicroservicePipeline <a name="ThronLambdaMicroservicePipeline" id="cdk-constructs.ThronLambdaMicroservicePipeline"></a>

Construct creating a multi environment pipeline.

*Example*

```typescript
  const projectId: string = `productsynctest`;
  const prefix: string = projectId;

  // Construct a custom image to be used for the build
  const defaultBuildImage: IBuildImage = ThronLambdaMicroservicePipeline.buildImageFromDockerfile(
    this,
    `${prefix}-cicd-build-docker`,
    path.join(__dirname, `../Docker/build-image`)
  );

  // Import an image from another repo
  const superSpecialImage: IBuildImage = ThronLambdaMicroservicePipeline.buildImageFromRepository(
    this,
    `super-special-repo`,
    `v1.2.1`
  );

  // Pipeline Instantiation
  const testConstruct = new ThronLambdaMicroservicePipeline(this, `${prefix}-cicd-pipeline-project`, {
    projectId,
    customBuildImage: defaultBuildImage,
    preExistingArtifactBucket: `very-special-bucket`,
    lambdas: {
      eventemitter: {},
      http: {},
      importprocessing: {},
      // Step with additional env variables
      importvalidation: {
        environmentalVariables: {
          specialVar: { value: `YEAH` }
        }
      },
      export: {}
    },
    tests: {
      // Step with custom build image
      Docs: { customBuildImage: superSpecialImage },
      Lint: {},
      // Step with more powerful build container
      Vuln: { computeType: ComputeType.MEDIUM },
      TestUnit: {},
      TestIntegration: {}
    },
    cicdConfig: {
      development: {
        capabilities: [
          PipelineCapability.BUILD,
          PipelineCapability.TEST,
          PipelineCapability.NOTIFY_ON_START,
          PipelineCapability.NOTIFY_ON_FAIL,
          PipelineCapability.NOTIFY_ON_SUCCESS
        ],
        webhookUrl: "https://example.com"
      },
      quality: {
        capabilities: [
          PipelineCapability.BUILD,
          PipelineCapability.NOTIFY_ON_SUCCESS
        ],
      },
    }
  });
```


#### Initializers <a name="Initializers" id="cdk-constructs.ThronLambdaMicroservicePipeline.Initializer"></a>

```typescript
import { ThronLambdaMicroservicePipeline } from 'cdk-constructs'

new ThronLambdaMicroservicePipeline(scope: Construct, id: string, props: ThronLambdaMicroservicePipelineProps)
```

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.ThronLambdaMicroservicePipeline.Initializer.parameter.scope">scope</a></code> | <code>constructs.Construct</code> | *No description.* |
| <code><a href="#cdk-constructs.ThronLambdaMicroservicePipeline.Initializer.parameter.id">id</a></code> | <code>string</code> | *No description.* |
| <code><a href="#cdk-constructs.ThronLambdaMicroservicePipeline.Initializer.parameter.props">props</a></code> | <code><a href="#cdk-constructs.ThronLambdaMicroservicePipelineProps">ThronLambdaMicroservicePipelineProps</a></code> | *No description.* |

---

##### `scope`<sup>Required</sup> <a name="scope" id="cdk-constructs.ThronLambdaMicroservicePipeline.Initializer.parameter.scope"></a>

- *Type:* constructs.Construct

---

##### `id`<sup>Required</sup> <a name="id" id="cdk-constructs.ThronLambdaMicroservicePipeline.Initializer.parameter.id"></a>

- *Type:* string

---

##### `props`<sup>Required</sup> <a name="props" id="cdk-constructs.ThronLambdaMicroservicePipeline.Initializer.parameter.props"></a>

- *Type:* <a href="#cdk-constructs.ThronLambdaMicroservicePipelineProps">ThronLambdaMicroservicePipelineProps</a>

---

#### Methods <a name="Methods" id="Methods"></a>

| **Name** | **Description** |
| --- | --- |
| <code><a href="#cdk-constructs.ThronLambdaMicroservicePipeline.toString">toString</a></code> | Returns a string representation of this construct. |

---

##### `toString` <a name="toString" id="cdk-constructs.ThronLambdaMicroservicePipeline.toString"></a>

```typescript
public toString(): string
```

Returns a string representation of this construct.

#### Static Functions <a name="Static Functions" id="Static Functions"></a>

| **Name** | **Description** |
| --- | --- |
| <code><a href="#cdk-constructs.ThronLambdaMicroservicePipeline.isConstruct">isConstruct</a></code> | Checks if `x` is a construct. |
| <code><a href="#cdk-constructs.ThronLambdaMicroservicePipeline.buildImageFromDockerfile">buildImageFromDockerfile</a></code> | *No description.* |
| <code><a href="#cdk-constructs.ThronLambdaMicroservicePipeline.buildImageFromRepository">buildImageFromRepository</a></code> | Constructs a Build Image to be used in the pipeline steps. |

---

##### `isConstruct` <a name="isConstruct" id="cdk-constructs.ThronLambdaMicroservicePipeline.isConstruct"></a>

```typescript
import { ThronLambdaMicroservicePipeline } from 'cdk-constructs'

ThronLambdaMicroservicePipeline.isConstruct(x: any)
```

Checks if `x` is a construct.

Use this method instead of `instanceof` to properly detect `Construct`
instances, even when the construct library is symlinked.

Explanation: in JavaScript, multiple copies of the `constructs` library on
disk are seen as independent, completely different libraries. As a
consequence, the class `Construct` in each copy of the `constructs` library
is seen as a different class, and an instance of one class will not test as
`instanceof` the other class. `npm install` will not create installations
like this, but users may manually symlink construct libraries together or
use a monorepo tool: in those cases, multiple copies of the `constructs`
library can be accidentally installed, and `instanceof` will behave
unpredictably. It is safest to avoid using `instanceof`, and using
this type-testing method instead.

###### `x`<sup>Required</sup> <a name="x" id="cdk-constructs.ThronLambdaMicroservicePipeline.isConstruct.parameter.x"></a>

- *Type:* any

Any object.

---

##### `buildImageFromDockerfile` <a name="buildImageFromDockerfile" id="cdk-constructs.ThronLambdaMicroservicePipeline.buildImageFromDockerfile"></a>

```typescript
import { ThronLambdaMicroservicePipeline } from 'cdk-constructs'

ThronLambdaMicroservicePipeline.buildImageFromDockerfile(scope: Construct, repositoryName: string, dockerfilePath: string)
```

###### `scope`<sup>Required</sup> <a name="scope" id="cdk-constructs.ThronLambdaMicroservicePipeline.buildImageFromDockerfile.parameter.scope"></a>

- *Type:* constructs.Construct

CDK scope to generate the construct in.

---

###### `repositoryName`<sup>Required</sup> <a name="repositoryName" id="cdk-constructs.ThronLambdaMicroservicePipeline.buildImageFromDockerfile.parameter.repositoryName"></a>

- *Type:* string

Name of the repository that will be created to host the image in.

---

###### `dockerfilePath`<sup>Required</sup> <a name="dockerfilePath" id="cdk-constructs.ThronLambdaMicroservicePipeline.buildImageFromDockerfile.parameter.dockerfilePath"></a>

- *Type:* string

Path of the docker file to build.

---

##### `buildImageFromRepository` <a name="buildImageFromRepository" id="cdk-constructs.ThronLambdaMicroservicePipeline.buildImageFromRepository"></a>

```typescript
import { ThronLambdaMicroservicePipeline } from 'cdk-constructs'

ThronLambdaMicroservicePipeline.buildImageFromRepository(scope: Construct, repositoryName: string, imageTag?: string)
```

Constructs a Build Image to be used in the pipeline steps.

###### `scope`<sup>Required</sup> <a name="scope" id="cdk-constructs.ThronLambdaMicroservicePipeline.buildImageFromRepository.parameter.scope"></a>

- *Type:* constructs.Construct

CDK scope to generate the construct in.

---

###### `repositoryName`<sup>Required</sup> <a name="repositoryName" id="cdk-constructs.ThronLambdaMicroservicePipeline.buildImageFromRepository.parameter.repositoryName"></a>

- *Type:* string

Name of the private repository to pull the image from.

---

###### `imageTag`<sup>Optional</sup> <a name="imageTag" id="cdk-constructs.ThronLambdaMicroservicePipeline.buildImageFromRepository.parameter.imageTag"></a>

- *Type:* string

Tag of the image.

Defaults to `latest`

---

#### Properties <a name="Properties" id="Properties"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.ThronLambdaMicroservicePipeline.property.node">node</a></code> | <code>constructs.Node</code> | The tree node. |
| <code><a href="#cdk-constructs.ThronLambdaMicroservicePipeline.property.pipelines">pipelines</a></code> | <code>{[ key: string ]: <a href="#cdk-constructs.ThronLambdaSingleEnvPipeline">ThronLambdaSingleEnvPipeline</a>}</code> | *No description.* |

---

##### `node`<sup>Required</sup> <a name="node" id="cdk-constructs.ThronLambdaMicroservicePipeline.property.node"></a>

```typescript
public readonly node: Node;
```

- *Type:* constructs.Node

The tree node.

---

##### `pipelines`<sup>Required</sup> <a name="pipelines" id="cdk-constructs.ThronLambdaMicroservicePipeline.property.pipelines"></a>

```typescript
public readonly pipelines: {[ key: string ]: ThronLambdaSingleEnvPipeline};
```

- *Type:* {[ key: string ]: <a href="#cdk-constructs.ThronLambdaSingleEnvPipeline">ThronLambdaSingleEnvPipeline</a>}

---

#### Constants <a name="Constants" id="Constants"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.ThronLambdaMicroservicePipeline.property.DeployConfigs">DeployConfigs</a></code> | <code>{[ key: string ]: <a href="#cdk-constructs.EnvironmentConfig">EnvironmentConfig</a>}</code> | Static and hardcoded deploy configs for the various environments. |

---

##### `DeployConfigs`<sup>Required</sup> <a name="DeployConfigs" id="cdk-constructs.ThronLambdaMicroservicePipeline.property.DeployConfigs"></a>

```typescript
public readonly DeployConfigs: {[ key: string ]: EnvironmentConfig};
```

- *Type:* {[ key: string ]: <a href="#cdk-constructs.EnvironmentConfig">EnvironmentConfig</a>}

Static and hardcoded deploy configs for the various environments.

---

### ThronLambdaSingleEnvPipeline <a name="ThronLambdaSingleEnvPipeline" id="cdk-constructs.ThronLambdaSingleEnvPipeline"></a>

- *Implements:* aws-cdk-lib.aws_iam.IGrantable

Class instantiating a pipeline for a single environment.

Depending on its configuration one might
- Enable or disable the `TEST` Stage
- Enable or disable the `BUILD` Stage
- Enable or disable MsTeams Notifications on various pipeline state change. See {@link PipelineCapability} for more
You should create `ThronLambdaSingleEnvPipeline` instances via the {@link ThronLambdaSingleEnvPipelineBuilder} builder class

#### Initializers <a name="Initializers" id="cdk-constructs.ThronLambdaSingleEnvPipeline.Initializer"></a>

```typescript
import { ThronLambdaSingleEnvPipeline } from 'cdk-constructs'

new ThronLambdaSingleEnvPipeline(scope: Construct, id: string, props: ThronLambdaSingleEnvPipelineProps)
```

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.ThronLambdaSingleEnvPipeline.Initializer.parameter.scope">scope</a></code> | <code>constructs.Construct</code> | *No description.* |
| <code><a href="#cdk-constructs.ThronLambdaSingleEnvPipeline.Initializer.parameter.id">id</a></code> | <code>string</code> | *No description.* |
| <code><a href="#cdk-constructs.ThronLambdaSingleEnvPipeline.Initializer.parameter.props">props</a></code> | <code><a href="#cdk-constructs.ThronLambdaSingleEnvPipelineProps">ThronLambdaSingleEnvPipelineProps</a></code> | *No description.* |

---

##### `scope`<sup>Required</sup> <a name="scope" id="cdk-constructs.ThronLambdaSingleEnvPipeline.Initializer.parameter.scope"></a>

- *Type:* constructs.Construct

---

##### `id`<sup>Required</sup> <a name="id" id="cdk-constructs.ThronLambdaSingleEnvPipeline.Initializer.parameter.id"></a>

- *Type:* string

---

##### `props`<sup>Required</sup> <a name="props" id="cdk-constructs.ThronLambdaSingleEnvPipeline.Initializer.parameter.props"></a>

- *Type:* <a href="#cdk-constructs.ThronLambdaSingleEnvPipelineProps">ThronLambdaSingleEnvPipelineProps</a>

---

#### Methods <a name="Methods" id="Methods"></a>

| **Name** | **Description** |
| --- | --- |
| <code><a href="#cdk-constructs.ThronLambdaSingleEnvPipeline.toString">toString</a></code> | Returns a string representation of this construct. |
| <code><a href="#cdk-constructs.ThronLambdaSingleEnvPipeline.addNotifyLambda">addNotifyLambda</a></code> | *No description.* |
| <code><a href="#cdk-constructs.ThronLambdaSingleEnvPipeline.generateBuildSteps">generateBuildSteps</a></code> | *No description.* |
| <code><a href="#cdk-constructs.ThronLambdaSingleEnvPipeline.generateDeploySteps">generateDeploySteps</a></code> | *No description.* |
| <code><a href="#cdk-constructs.ThronLambdaSingleEnvPipeline.generateTestSteps">generateTestSteps</a></code> | *No description.* |

---

##### `toString` <a name="toString" id="cdk-constructs.ThronLambdaSingleEnvPipeline.toString"></a>

```typescript
public toString(): string
```

Returns a string representation of this construct.

##### `addNotifyLambda` <a name="addNotifyLambda" id="cdk-constructs.ThronLambdaSingleEnvPipeline.addNotifyLambda"></a>

```typescript
public addNotifyLambda(props: ThronLambdaSingleEnvPipelineProps, pipeline: Pipeline): void
```

###### `props`<sup>Required</sup> <a name="props" id="cdk-constructs.ThronLambdaSingleEnvPipeline.addNotifyLambda.parameter.props"></a>

- *Type:* <a href="#cdk-constructs.ThronLambdaSingleEnvPipelineProps">ThronLambdaSingleEnvPipelineProps</a>

---

###### `pipeline`<sup>Required</sup> <a name="pipeline" id="cdk-constructs.ThronLambdaSingleEnvPipeline.addNotifyLambda.parameter.pipeline"></a>

- *Type:* aws-cdk-lib.aws_codepipeline.Pipeline

---

##### `generateBuildSteps` <a name="generateBuildSteps" id="cdk-constructs.ThronLambdaSingleEnvPipeline.generateBuildSteps"></a>

```typescript
public generateBuildSteps(props: ThronLambdaSingleEnvPipelineProps, stageName: string): StageProducts
```

###### `props`<sup>Required</sup> <a name="props" id="cdk-constructs.ThronLambdaSingleEnvPipeline.generateBuildSteps.parameter.props"></a>

- *Type:* <a href="#cdk-constructs.ThronLambdaSingleEnvPipelineProps">ThronLambdaSingleEnvPipelineProps</a>

---

###### `stageName`<sup>Required</sup> <a name="stageName" id="cdk-constructs.ThronLambdaSingleEnvPipeline.generateBuildSteps.parameter.stageName"></a>

- *Type:* string

---

##### `generateDeploySteps` <a name="generateDeploySteps" id="cdk-constructs.ThronLambdaSingleEnvPipeline.generateDeploySteps"></a>

```typescript
public generateDeploySteps(props: ThronLambdaSingleEnvPipelineProps, stageName: string): StageProducts
```

###### `props`<sup>Required</sup> <a name="props" id="cdk-constructs.ThronLambdaSingleEnvPipeline.generateDeploySteps.parameter.props"></a>

- *Type:* <a href="#cdk-constructs.ThronLambdaSingleEnvPipelineProps">ThronLambdaSingleEnvPipelineProps</a>

---

###### `stageName`<sup>Required</sup> <a name="stageName" id="cdk-constructs.ThronLambdaSingleEnvPipeline.generateDeploySteps.parameter.stageName"></a>

- *Type:* string

---

##### `generateTestSteps` <a name="generateTestSteps" id="cdk-constructs.ThronLambdaSingleEnvPipeline.generateTestSteps"></a>

```typescript
public generateTestSteps(props: ThronLambdaSingleEnvPipelineProps, stageName: string): StageProducts
```

###### `props`<sup>Required</sup> <a name="props" id="cdk-constructs.ThronLambdaSingleEnvPipeline.generateTestSteps.parameter.props"></a>

- *Type:* <a href="#cdk-constructs.ThronLambdaSingleEnvPipelineProps">ThronLambdaSingleEnvPipelineProps</a>

---

###### `stageName`<sup>Required</sup> <a name="stageName" id="cdk-constructs.ThronLambdaSingleEnvPipeline.generateTestSteps.parameter.stageName"></a>

- *Type:* string

---

#### Static Functions <a name="Static Functions" id="Static Functions"></a>

| **Name** | **Description** |
| --- | --- |
| <code><a href="#cdk-constructs.ThronLambdaSingleEnvPipeline.isConstruct">isConstruct</a></code> | Checks if `x` is a construct. |

---

##### `isConstruct` <a name="isConstruct" id="cdk-constructs.ThronLambdaSingleEnvPipeline.isConstruct"></a>

```typescript
import { ThronLambdaSingleEnvPipeline } from 'cdk-constructs'

ThronLambdaSingleEnvPipeline.isConstruct(x: any)
```

Checks if `x` is a construct.

Use this method instead of `instanceof` to properly detect `Construct`
instances, even when the construct library is symlinked.

Explanation: in JavaScript, multiple copies of the `constructs` library on
disk are seen as independent, completely different libraries. As a
consequence, the class `Construct` in each copy of the `constructs` library
is seen as a different class, and an instance of one class will not test as
`instanceof` the other class. `npm install` will not create installations
like this, but users may manually symlink construct libraries together or
use a monorepo tool: in those cases, multiple copies of the `constructs`
library can be accidentally installed, and `instanceof` will behave
unpredictably. It is safest to avoid using `instanceof`, and using
this type-testing method instead.

###### `x`<sup>Required</sup> <a name="x" id="cdk-constructs.ThronLambdaSingleEnvPipeline.isConstruct.parameter.x"></a>

- *Type:* any

Any object.

---

#### Properties <a name="Properties" id="Properties"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.ThronLambdaSingleEnvPipeline.property.node">node</a></code> | <code>constructs.Node</code> | The tree node. |
| <code><a href="#cdk-constructs.ThronLambdaSingleEnvPipeline.property.grantPrincipal">grantPrincipal</a></code> | <code>aws-cdk-lib.aws_iam.IPrincipal</code> | The principal to grant permissions to. |

---

##### `node`<sup>Required</sup> <a name="node" id="cdk-constructs.ThronLambdaSingleEnvPipeline.property.node"></a>

```typescript
public readonly node: Node;
```

- *Type:* constructs.Node

The tree node.

---

##### `grantPrincipal`<sup>Required</sup> <a name="grantPrincipal" id="cdk-constructs.ThronLambdaSingleEnvPipeline.property.grantPrincipal"></a>

```typescript
public readonly grantPrincipal: IPrincipal;
```

- *Type:* aws-cdk-lib.aws_iam.IPrincipal

The principal to grant permissions to.

---


### ThronNewRelicContextInjector <a name="ThronNewRelicContextInjector" id="cdk-constructs.ThronNewRelicContextInjector"></a>

A construct that injects NewRelic configuration into a Lambda function.

#### Initializers <a name="Initializers" id="cdk-constructs.ThronNewRelicContextInjector.Initializer"></a>

```typescript
import { ThronNewRelicContextInjector } from 'cdk-constructs'

new ThronNewRelicContextInjector(scope: Construct, id: string, props: ThronNewRelicContextInjectorOptions)
```

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.ThronNewRelicContextInjector.Initializer.parameter.scope">scope</a></code> | <code>constructs.Construct</code> | - The scope in which this construct is defined. |
| <code><a href="#cdk-constructs.ThronNewRelicContextInjector.Initializer.parameter.id">id</a></code> | <code>string</code> | - The scoped construct ID. |
| <code><a href="#cdk-constructs.ThronNewRelicContextInjector.Initializer.parameter.props">props</a></code> | <code><a href="#cdk-constructs.ThronNewRelicContextInjectorOptions">ThronNewRelicContextInjectorOptions</a></code> | - The NewRelic configuration options. |

---

##### `scope`<sup>Required</sup> <a name="scope" id="cdk-constructs.ThronNewRelicContextInjector.Initializer.parameter.scope"></a>

- *Type:* constructs.Construct

The scope in which this construct is defined.

---

##### `id`<sup>Required</sup> <a name="id" id="cdk-constructs.ThronNewRelicContextInjector.Initializer.parameter.id"></a>

- *Type:* string

The scoped construct ID.

---

##### `props`<sup>Required</sup> <a name="props" id="cdk-constructs.ThronNewRelicContextInjector.Initializer.parameter.props"></a>

- *Type:* <a href="#cdk-constructs.ThronNewRelicContextInjectorOptions">ThronNewRelicContextInjectorOptions</a>

The NewRelic configuration options.

---

#### Methods <a name="Methods" id="Methods"></a>

| **Name** | **Description** |
| --- | --- |
| <code><a href="#cdk-constructs.ThronNewRelicContextInjector.toString">toString</a></code> | Returns a string representation of this construct. |
| <code><a href="#cdk-constructs.ThronNewRelicContextInjector.injectEnvironment">injectEnvironment</a></code> | Injects the NewRelic environment variables into the given Lambda function. |

---

##### `toString` <a name="toString" id="cdk-constructs.ThronNewRelicContextInjector.toString"></a>

```typescript
public toString(): string
```

Returns a string representation of this construct.

##### `injectEnvironment` <a name="injectEnvironment" id="cdk-constructs.ThronNewRelicContextInjector.injectEnvironment"></a>

```typescript
public injectEnvironment(lambdaFunction: Function): void
```

Injects the NewRelic environment variables into the given Lambda function.

###### `lambdaFunction`<sup>Required</sup> <a name="lambdaFunction" id="cdk-constructs.ThronNewRelicContextInjector.injectEnvironment.parameter.lambdaFunction"></a>

- *Type:* aws-cdk-lib.aws_lambda.Function

The Lambda function to inject the environment variables into.

---

#### Static Functions <a name="Static Functions" id="Static Functions"></a>

| **Name** | **Description** |
| --- | --- |
| <code><a href="#cdk-constructs.ThronNewRelicContextInjector.isConstruct">isConstruct</a></code> | Checks if `x` is a construct. |

---

##### `isConstruct` <a name="isConstruct" id="cdk-constructs.ThronNewRelicContextInjector.isConstruct"></a>

```typescript
import { ThronNewRelicContextInjector } from 'cdk-constructs'

ThronNewRelicContextInjector.isConstruct(x: any)
```

Checks if `x` is a construct.

Use this method instead of `instanceof` to properly detect `Construct`
instances, even when the construct library is symlinked.

Explanation: in JavaScript, multiple copies of the `constructs` library on
disk are seen as independent, completely different libraries. As a
consequence, the class `Construct` in each copy of the `constructs` library
is seen as a different class, and an instance of one class will not test as
`instanceof` the other class. `npm install` will not create installations
like this, but users may manually symlink construct libraries together or
use a monorepo tool: in those cases, multiple copies of the `constructs`
library can be accidentally installed, and `instanceof` will behave
unpredictably. It is safest to avoid using `instanceof`, and using
this type-testing method instead.

###### `x`<sup>Required</sup> <a name="x" id="cdk-constructs.ThronNewRelicContextInjector.isConstruct.parameter.x"></a>

- *Type:* any

Any object.

---

#### Properties <a name="Properties" id="Properties"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.ThronNewRelicContextInjector.property.node">node</a></code> | <code>constructs.Node</code> | The tree node. |
| <code><a href="#cdk-constructs.ThronNewRelicContextInjector.property.newRelicEnvironment">newRelicEnvironment</a></code> | <code>{[ key: string ]: string}</code> | *No description.* |

---

##### `node`<sup>Required</sup> <a name="node" id="cdk-constructs.ThronNewRelicContextInjector.property.node"></a>

```typescript
public readonly node: Node;
```

- *Type:* constructs.Node

The tree node.

---

##### `newRelicEnvironment`<sup>Required</sup> <a name="newRelicEnvironment" id="cdk-constructs.ThronNewRelicContextInjector.property.newRelicEnvironment"></a>

```typescript
public readonly newRelicEnvironment: {[ key: string ]: string};
```

- *Type:* {[ key: string ]: string}

---


### ThronNewRelicDockerLambda <a name="ThronNewRelicDockerLambda" id="cdk-constructs.ThronNewRelicDockerLambda"></a>

A Lambda Docker function with NewRelic integration.

#### Initializers <a name="Initializers" id="cdk-constructs.ThronNewRelicDockerLambda.Initializer"></a>

```typescript
import { ThronNewRelicDockerLambda } from 'cdk-constructs'

new ThronNewRelicDockerLambda(scope: Stack, id: string, props: NewRelicFunctionOptions)
```

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.ThronNewRelicDockerLambda.Initializer.parameter.scope">scope</a></code> | <code>aws-cdk-lib.Stack</code> | - The scope in which this construct is defined. |
| <code><a href="#cdk-constructs.ThronNewRelicDockerLambda.Initializer.parameter.id">id</a></code> | <code>string</code> | - The scoped construct ID. |
| <code><a href="#cdk-constructs.ThronNewRelicDockerLambda.Initializer.parameter.props">props</a></code> | <code><a href="#cdk-constructs.NewRelicFunctionOptions">NewRelicFunctionOptions</a></code> | - The function properties including NewRelic configuration overrides. |

---

##### `scope`<sup>Required</sup> <a name="scope" id="cdk-constructs.ThronNewRelicDockerLambda.Initializer.parameter.scope"></a>

- *Type:* aws-cdk-lib.Stack

The scope in which this construct is defined.

---

##### `id`<sup>Required</sup> <a name="id" id="cdk-constructs.ThronNewRelicDockerLambda.Initializer.parameter.id"></a>

- *Type:* string

The scoped construct ID.

---

##### `props`<sup>Required</sup> <a name="props" id="cdk-constructs.ThronNewRelicDockerLambda.Initializer.parameter.props"></a>

- *Type:* <a href="#cdk-constructs.NewRelicFunctionOptions">NewRelicFunctionOptions</a>

The function properties including NewRelic configuration overrides.

---

#### Methods <a name="Methods" id="Methods"></a>

| **Name** | **Description** |
| --- | --- |
| <code><a href="#cdk-constructs.ThronNewRelicDockerLambda.toString">toString</a></code> | Returns a string representation of this construct. |
| <code><a href="#cdk-constructs.ThronNewRelicDockerLambda.applyRemovalPolicy">applyRemovalPolicy</a></code> | Apply the given removal policy to this resource. |
| <code><a href="#cdk-constructs.ThronNewRelicDockerLambda.addEventSource">addEventSource</a></code> | Adds an event source to this function. |
| <code><a href="#cdk-constructs.ThronNewRelicDockerLambda.addEventSourceMapping">addEventSourceMapping</a></code> | Adds an event source that maps to this AWS Lambda function. |
| <code><a href="#cdk-constructs.ThronNewRelicDockerLambda.addFunctionUrl">addFunctionUrl</a></code> | Adds a url to this lambda function. |
| <code><a href="#cdk-constructs.ThronNewRelicDockerLambda.addPermission">addPermission</a></code> | Adds a permission to the Lambda resource policy. |
| <code><a href="#cdk-constructs.ThronNewRelicDockerLambda.addToRolePolicy">addToRolePolicy</a></code> | Adds a statement to the IAM role assumed by the instance. |
| <code><a href="#cdk-constructs.ThronNewRelicDockerLambda.configureAsyncInvoke">configureAsyncInvoke</a></code> | Configures options for asynchronous invocation. |
| <code><a href="#cdk-constructs.ThronNewRelicDockerLambda.considerWarningOnInvokeFunctionPermissions">considerWarningOnInvokeFunctionPermissions</a></code> | A warning will be added to functions under the following conditions: - permissions that include `lambda:InvokeFunction` are added to the unqualified function. |
| <code><a href="#cdk-constructs.ThronNewRelicDockerLambda.grantInvoke">grantInvoke</a></code> | Grant the given identity permissions to invoke this Lambda. |
| <code><a href="#cdk-constructs.ThronNewRelicDockerLambda.grantInvokeCompositePrincipal">grantInvokeCompositePrincipal</a></code> | Grant multiple principals the ability to invoke this Lambda via CompositePrincipal. |
| <code><a href="#cdk-constructs.ThronNewRelicDockerLambda.grantInvokeLatestVersion">grantInvokeLatestVersion</a></code> | Grant the given identity permissions to invoke the $LATEST version or unqualified version of this Lambda. |
| <code><a href="#cdk-constructs.ThronNewRelicDockerLambda.grantInvokeUrl">grantInvokeUrl</a></code> | Grant the given identity permissions to invoke this Lambda Function URL. |
| <code><a href="#cdk-constructs.ThronNewRelicDockerLambda.grantInvokeVersion">grantInvokeVersion</a></code> | Grant the given identity permissions to invoke the given version of this Lambda. |
| <code><a href="#cdk-constructs.ThronNewRelicDockerLambda.metric">metric</a></code> | Return the given named metric for this Function. |
| <code><a href="#cdk-constructs.ThronNewRelicDockerLambda.metricDuration">metricDuration</a></code> | How long execution of this Lambda takes. |
| <code><a href="#cdk-constructs.ThronNewRelicDockerLambda.metricErrors">metricErrors</a></code> | How many invocations of this Lambda fail. |
| <code><a href="#cdk-constructs.ThronNewRelicDockerLambda.metricInvocations">metricInvocations</a></code> | How often this Lambda is invoked. |
| <code><a href="#cdk-constructs.ThronNewRelicDockerLambda.metricThrottles">metricThrottles</a></code> | How often this Lambda is throttled. |
| <code><a href="#cdk-constructs.ThronNewRelicDockerLambda.addAlias">addAlias</a></code> | Defines an alias for this function. |
| <code><a href="#cdk-constructs.ThronNewRelicDockerLambda.addEnvironment">addEnvironment</a></code> | Adds an environment variable to this Lambda function. |
| <code><a href="#cdk-constructs.ThronNewRelicDockerLambda.addLayers">addLayers</a></code> | Adds one or more Lambda Layers to this Lambda function. |
| <code><a href="#cdk-constructs.ThronNewRelicDockerLambda.invalidateVersionBasedOn">invalidateVersionBasedOn</a></code> | Mix additional information into the hash of the Version object. |
| <code><a href="#cdk-constructs.ThronNewRelicDockerLambda.addEndpointAlb">addEndpointAlb</a></code> | Add an endpoint the lambda function. |
| <code><a href="#cdk-constructs.ThronNewRelicDockerLambda.addLegacyEndpointAlb">addLegacyEndpointAlb</a></code> | Add a legacy endpoint to the lambda function. |

---

##### `toString` <a name="toString" id="cdk-constructs.ThronNewRelicDockerLambda.toString"></a>

```typescript
public toString(): string
```

Returns a string representation of this construct.

##### `applyRemovalPolicy` <a name="applyRemovalPolicy" id="cdk-constructs.ThronNewRelicDockerLambda.applyRemovalPolicy"></a>

```typescript
public applyRemovalPolicy(policy: RemovalPolicy): void
```

Apply the given removal policy to this resource.

The Removal Policy controls what happens to this resource when it stops
being managed by CloudFormation, either because you've removed it from the
CDK application or because you've made a change that requires the resource
to be replaced.

The resource can be deleted (`RemovalPolicy.DESTROY`), or left in your AWS
account for data recovery and cleanup later (`RemovalPolicy.RETAIN`).

###### `policy`<sup>Required</sup> <a name="policy" id="cdk-constructs.ThronNewRelicDockerLambda.applyRemovalPolicy.parameter.policy"></a>

- *Type:* aws-cdk-lib.RemovalPolicy

---

##### `addEventSource` <a name="addEventSource" id="cdk-constructs.ThronNewRelicDockerLambda.addEventSource"></a>

```typescript
public addEventSource(source: IEventSource): void
```

Adds an event source to this function.

Event sources are implemented in the aws-cdk-lib/aws-lambda-event-sources module.

The following example adds an SQS Queue as an event source:
```
import { SqsEventSource } from 'aws-cdk-lib/aws-lambda-event-sources';
myFunction.addEventSource(new SqsEventSource(myQueue));
```

###### `source`<sup>Required</sup> <a name="source" id="cdk-constructs.ThronNewRelicDockerLambda.addEventSource.parameter.source"></a>

- *Type:* aws-cdk-lib.aws_lambda.IEventSource

---

##### `addEventSourceMapping` <a name="addEventSourceMapping" id="cdk-constructs.ThronNewRelicDockerLambda.addEventSourceMapping"></a>

```typescript
public addEventSourceMapping(id: string, options: EventSourceMappingOptions): EventSourceMapping
```

Adds an event source that maps to this AWS Lambda function.

###### `id`<sup>Required</sup> <a name="id" id="cdk-constructs.ThronNewRelicDockerLambda.addEventSourceMapping.parameter.id"></a>

- *Type:* string

---

###### `options`<sup>Required</sup> <a name="options" id="cdk-constructs.ThronNewRelicDockerLambda.addEventSourceMapping.parameter.options"></a>

- *Type:* aws-cdk-lib.aws_lambda.EventSourceMappingOptions

---

##### `addFunctionUrl` <a name="addFunctionUrl" id="cdk-constructs.ThronNewRelicDockerLambda.addFunctionUrl"></a>

```typescript
public addFunctionUrl(options?: FunctionUrlOptions): FunctionUrl
```

Adds a url to this lambda function.

###### `options`<sup>Optional</sup> <a name="options" id="cdk-constructs.ThronNewRelicDockerLambda.addFunctionUrl.parameter.options"></a>

- *Type:* aws-cdk-lib.aws_lambda.FunctionUrlOptions

---

##### `addPermission` <a name="addPermission" id="cdk-constructs.ThronNewRelicDockerLambda.addPermission"></a>

```typescript
public addPermission(id: string, permission: Permission): void
```

Adds a permission to the Lambda resource policy.

> [Permission for details.](Permission for details.)

###### `id`<sup>Required</sup> <a name="id" id="cdk-constructs.ThronNewRelicDockerLambda.addPermission.parameter.id"></a>

- *Type:* string

The id for the permission construct.

---

###### `permission`<sup>Required</sup> <a name="permission" id="cdk-constructs.ThronNewRelicDockerLambda.addPermission.parameter.permission"></a>

- *Type:* aws-cdk-lib.aws_lambda.Permission

The permission to grant to this Lambda function.

---

##### `addToRolePolicy` <a name="addToRolePolicy" id="cdk-constructs.ThronNewRelicDockerLambda.addToRolePolicy"></a>

```typescript
public addToRolePolicy(statement: PolicyStatement): void
```

Adds a statement to the IAM role assumed by the instance.

###### `statement`<sup>Required</sup> <a name="statement" id="cdk-constructs.ThronNewRelicDockerLambda.addToRolePolicy.parameter.statement"></a>

- *Type:* aws-cdk-lib.aws_iam.PolicyStatement

---

##### `configureAsyncInvoke` <a name="configureAsyncInvoke" id="cdk-constructs.ThronNewRelicDockerLambda.configureAsyncInvoke"></a>

```typescript
public configureAsyncInvoke(options: EventInvokeConfigOptions): void
```

Configures options for asynchronous invocation.

###### `options`<sup>Required</sup> <a name="options" id="cdk-constructs.ThronNewRelicDockerLambda.configureAsyncInvoke.parameter.options"></a>

- *Type:* aws-cdk-lib.aws_lambda.EventInvokeConfigOptions

---

##### `considerWarningOnInvokeFunctionPermissions` <a name="considerWarningOnInvokeFunctionPermissions" id="cdk-constructs.ThronNewRelicDockerLambda.considerWarningOnInvokeFunctionPermissions"></a>

```typescript
public considerWarningOnInvokeFunctionPermissions(scope: Construct, action: string): void
```

A warning will be added to functions under the following conditions: - permissions that include `lambda:InvokeFunction` are added to the unqualified function.

function.currentVersion is invoked before or after the permission is created.

This applies only to permissions on Lambda functions, not versions or aliases.
This function is overridden as a noOp for QualifiedFunctionBase.

###### `scope`<sup>Required</sup> <a name="scope" id="cdk-constructs.ThronNewRelicDockerLambda.considerWarningOnInvokeFunctionPermissions.parameter.scope"></a>

- *Type:* constructs.Construct

---

###### `action`<sup>Required</sup> <a name="action" id="cdk-constructs.ThronNewRelicDockerLambda.considerWarningOnInvokeFunctionPermissions.parameter.action"></a>

- *Type:* string

---

##### `grantInvoke` <a name="grantInvoke" id="cdk-constructs.ThronNewRelicDockerLambda.grantInvoke"></a>

```typescript
public grantInvoke(grantee: IGrantable): Grant
```

Grant the given identity permissions to invoke this Lambda.

###### `grantee`<sup>Required</sup> <a name="grantee" id="cdk-constructs.ThronNewRelicDockerLambda.grantInvoke.parameter.grantee"></a>

- *Type:* aws-cdk-lib.aws_iam.IGrantable

---

##### `grantInvokeCompositePrincipal` <a name="grantInvokeCompositePrincipal" id="cdk-constructs.ThronNewRelicDockerLambda.grantInvokeCompositePrincipal"></a>

```typescript
public grantInvokeCompositePrincipal(compositePrincipal: CompositePrincipal): Grant[]
```

Grant multiple principals the ability to invoke this Lambda via CompositePrincipal.

###### `compositePrincipal`<sup>Required</sup> <a name="compositePrincipal" id="cdk-constructs.ThronNewRelicDockerLambda.grantInvokeCompositePrincipal.parameter.compositePrincipal"></a>

- *Type:* aws-cdk-lib.aws_iam.CompositePrincipal

---

##### `grantInvokeLatestVersion` <a name="grantInvokeLatestVersion" id="cdk-constructs.ThronNewRelicDockerLambda.grantInvokeLatestVersion"></a>

```typescript
public grantInvokeLatestVersion(grantee: IGrantable): Grant
```

Grant the given identity permissions to invoke the $LATEST version or unqualified version of this Lambda.

###### `grantee`<sup>Required</sup> <a name="grantee" id="cdk-constructs.ThronNewRelicDockerLambda.grantInvokeLatestVersion.parameter.grantee"></a>

- *Type:* aws-cdk-lib.aws_iam.IGrantable

---

##### `grantInvokeUrl` <a name="grantInvokeUrl" id="cdk-constructs.ThronNewRelicDockerLambda.grantInvokeUrl"></a>

```typescript
public grantInvokeUrl(grantee: IGrantable): Grant
```

Grant the given identity permissions to invoke this Lambda Function URL.

###### `grantee`<sup>Required</sup> <a name="grantee" id="cdk-constructs.ThronNewRelicDockerLambda.grantInvokeUrl.parameter.grantee"></a>

- *Type:* aws-cdk-lib.aws_iam.IGrantable

---

##### `grantInvokeVersion` <a name="grantInvokeVersion" id="cdk-constructs.ThronNewRelicDockerLambda.grantInvokeVersion"></a>

```typescript
public grantInvokeVersion(grantee: IGrantable, version: IVersion): Grant
```

Grant the given identity permissions to invoke the given version of this Lambda.

###### `grantee`<sup>Required</sup> <a name="grantee" id="cdk-constructs.ThronNewRelicDockerLambda.grantInvokeVersion.parameter.grantee"></a>

- *Type:* aws-cdk-lib.aws_iam.IGrantable

---

###### `version`<sup>Required</sup> <a name="version" id="cdk-constructs.ThronNewRelicDockerLambda.grantInvokeVersion.parameter.version"></a>

- *Type:* aws-cdk-lib.aws_lambda.IVersion

---

##### `metric` <a name="metric" id="cdk-constructs.ThronNewRelicDockerLambda.metric"></a>

```typescript
public metric(metricName: string, props?: MetricOptions): Metric
```

Return the given named metric for this Function.

###### `metricName`<sup>Required</sup> <a name="metricName" id="cdk-constructs.ThronNewRelicDockerLambda.metric.parameter.metricName"></a>

- *Type:* string

---

###### `props`<sup>Optional</sup> <a name="props" id="cdk-constructs.ThronNewRelicDockerLambda.metric.parameter.props"></a>

- *Type:* aws-cdk-lib.aws_cloudwatch.MetricOptions

---

##### `metricDuration` <a name="metricDuration" id="cdk-constructs.ThronNewRelicDockerLambda.metricDuration"></a>

```typescript
public metricDuration(props?: MetricOptions): Metric
```

How long execution of this Lambda takes.

Average over 5 minutes

###### `props`<sup>Optional</sup> <a name="props" id="cdk-constructs.ThronNewRelicDockerLambda.metricDuration.parameter.props"></a>

- *Type:* aws-cdk-lib.aws_cloudwatch.MetricOptions

---

##### `metricErrors` <a name="metricErrors" id="cdk-constructs.ThronNewRelicDockerLambda.metricErrors"></a>

```typescript
public metricErrors(props?: MetricOptions): Metric
```

How many invocations of this Lambda fail.

Sum over 5 minutes

###### `props`<sup>Optional</sup> <a name="props" id="cdk-constructs.ThronNewRelicDockerLambda.metricErrors.parameter.props"></a>

- *Type:* aws-cdk-lib.aws_cloudwatch.MetricOptions

---

##### `metricInvocations` <a name="metricInvocations" id="cdk-constructs.ThronNewRelicDockerLambda.metricInvocations"></a>

```typescript
public metricInvocations(props?: MetricOptions): Metric
```

How often this Lambda is invoked.

Sum over 5 minutes

###### `props`<sup>Optional</sup> <a name="props" id="cdk-constructs.ThronNewRelicDockerLambda.metricInvocations.parameter.props"></a>

- *Type:* aws-cdk-lib.aws_cloudwatch.MetricOptions

---

##### `metricThrottles` <a name="metricThrottles" id="cdk-constructs.ThronNewRelicDockerLambda.metricThrottles"></a>

```typescript
public metricThrottles(props?: MetricOptions): Metric
```

How often this Lambda is throttled.

Sum over 5 minutes

###### `props`<sup>Optional</sup> <a name="props" id="cdk-constructs.ThronNewRelicDockerLambda.metricThrottles.parameter.props"></a>

- *Type:* aws-cdk-lib.aws_cloudwatch.MetricOptions

---

##### `addAlias` <a name="addAlias" id="cdk-constructs.ThronNewRelicDockerLambda.addAlias"></a>

```typescript
public addAlias(aliasName: string, options?: AliasOptions): Alias
```

Defines an alias for this function.

The alias will automatically be updated to point to the latest version of
the function as it is being updated during a deployment.

```ts
declare const fn: lambda.Function;

fn.addAlias('Live');

// Is equivalent to

new lambda.Alias(this, 'AliasLive', {
  aliasName: 'Live',
  version: fn.currentVersion,
});
```

###### `aliasName`<sup>Required</sup> <a name="aliasName" id="cdk-constructs.ThronNewRelicDockerLambda.addAlias.parameter.aliasName"></a>

- *Type:* string

The name of the alias.

---

###### `options`<sup>Optional</sup> <a name="options" id="cdk-constructs.ThronNewRelicDockerLambda.addAlias.parameter.options"></a>

- *Type:* aws-cdk-lib.aws_lambda.AliasOptions

Alias options.

---

##### `addEnvironment` <a name="addEnvironment" id="cdk-constructs.ThronNewRelicDockerLambda.addEnvironment"></a>

```typescript
public addEnvironment(key: string, value: string, options?: EnvironmentOptions): Function
```

Adds an environment variable to this Lambda function.

If this is a ref to a Lambda function, this operation results in a no-op.

###### `key`<sup>Required</sup> <a name="key" id="cdk-constructs.ThronNewRelicDockerLambda.addEnvironment.parameter.key"></a>

- *Type:* string

The environment variable key.

---

###### `value`<sup>Required</sup> <a name="value" id="cdk-constructs.ThronNewRelicDockerLambda.addEnvironment.parameter.value"></a>

- *Type:* string

The environment variable's value.

---

###### `options`<sup>Optional</sup> <a name="options" id="cdk-constructs.ThronNewRelicDockerLambda.addEnvironment.parameter.options"></a>

- *Type:* aws-cdk-lib.aws_lambda.EnvironmentOptions

Environment variable options.

---

##### `addLayers` <a name="addLayers" id="cdk-constructs.ThronNewRelicDockerLambda.addLayers"></a>

```typescript
public addLayers(layers: ILayerVersion): void
```

Adds one or more Lambda Layers to this Lambda function.

###### `layers`<sup>Required</sup> <a name="layers" id="cdk-constructs.ThronNewRelicDockerLambda.addLayers.parameter.layers"></a>

- *Type:* aws-cdk-lib.aws_lambda.ILayerVersion

the layers to be added.

---

##### `invalidateVersionBasedOn` <a name="invalidateVersionBasedOn" id="cdk-constructs.ThronNewRelicDockerLambda.invalidateVersionBasedOn"></a>

```typescript
public invalidateVersionBasedOn(x: string): void
```

Mix additional information into the hash of the Version object.

The Lambda Function construct does its best to automatically create a new
Version when anything about the Function changes (its code, its layers,
any of the other properties).

However, you can sometimes source information from places that the CDK cannot
look into, like the deploy-time values of SSM parameters. In those cases,
the CDK would not force the creation of a new Version object when it actually
should.

This method can be used to invalidate the current Version object. Pass in
any string into this method, and make sure the string changes when you know
a new Version needs to be created.

This method may be called more than once.

###### `x`<sup>Required</sup> <a name="x" id="cdk-constructs.ThronNewRelicDockerLambda.invalidateVersionBasedOn.parameter.x"></a>

- *Type:* string

---

##### `addEndpointAlb` <a name="addEndpointAlb" id="cdk-constructs.ThronNewRelicDockerLambda.addEndpointAlb"></a>

```typescript
public addEndpointAlb(name: string, endpointProps: ThronEndpointAlbProps): EndpointAlb
```

Add an endpoint the lambda function.

###### `name`<sup>Required</sup> <a name="name" id="cdk-constructs.ThronNewRelicDockerLambda.addEndpointAlb.parameter.name"></a>

- *Type:* string

---

###### `endpointProps`<sup>Required</sup> <a name="endpointProps" id="cdk-constructs.ThronNewRelicDockerLambda.addEndpointAlb.parameter.endpointProps"></a>

- *Type:* <a href="#cdk-constructs.ThronEndpointAlbProps">ThronEndpointAlbProps</a>

---

##### `addLegacyEndpointAlb` <a name="addLegacyEndpointAlb" id="cdk-constructs.ThronNewRelicDockerLambda.addLegacyEndpointAlb"></a>

```typescript
public addLegacyEndpointAlb(name: string, endpointProps: LegacyEndpointAlbProps): EndpointAlb
```

Add a legacy endpoint to the lambda function.

###### `name`<sup>Required</sup> <a name="name" id="cdk-constructs.ThronNewRelicDockerLambda.addLegacyEndpointAlb.parameter.name"></a>

- *Type:* string

---

###### `endpointProps`<sup>Required</sup> <a name="endpointProps" id="cdk-constructs.ThronNewRelicDockerLambda.addLegacyEndpointAlb.parameter.endpointProps"></a>

- *Type:* <a href="#cdk-constructs.LegacyEndpointAlbProps">LegacyEndpointAlbProps</a>

---

#### Static Functions <a name="Static Functions" id="Static Functions"></a>

| **Name** | **Description** |
| --- | --- |
| <code><a href="#cdk-constructs.ThronNewRelicDockerLambda.isConstruct">isConstruct</a></code> | Checks if `x` is a construct. |
| <code><a href="#cdk-constructs.ThronNewRelicDockerLambda.isOwnedResource">isOwnedResource</a></code> | Returns true if the construct was created by CDK, and false otherwise. |
| <code><a href="#cdk-constructs.ThronNewRelicDockerLambda.isResource">isResource</a></code> | Check whether the given construct is a Resource. |
| <code><a href="#cdk-constructs.ThronNewRelicDockerLambda.classifyVersionProperty">classifyVersionProperty</a></code> | Record whether specific properties in the `AWS::Lambda::Function` resource should also be associated to the Version resource. |
| <code><a href="#cdk-constructs.ThronNewRelicDockerLambda.fromFunctionArn">fromFunctionArn</a></code> | Import a lambda function into the CDK using its ARN. |
| <code><a href="#cdk-constructs.ThronNewRelicDockerLambda.fromFunctionAttributes">fromFunctionAttributes</a></code> | Creates a Lambda function object which represents a function not defined within this stack. |
| <code><a href="#cdk-constructs.ThronNewRelicDockerLambda.fromFunctionName">fromFunctionName</a></code> | Import a lambda function into the CDK using its name. |
| <code><a href="#cdk-constructs.ThronNewRelicDockerLambda.metricAll">metricAll</a></code> | Return the given named metric for this Lambda. |
| <code><a href="#cdk-constructs.ThronNewRelicDockerLambda.metricAllConcurrentExecutions">metricAllConcurrentExecutions</a></code> | Metric for the number of concurrent executions across all Lambdas. |
| <code><a href="#cdk-constructs.ThronNewRelicDockerLambda.metricAllDuration">metricAllDuration</a></code> | Metric for the Duration executing all Lambdas. |
| <code><a href="#cdk-constructs.ThronNewRelicDockerLambda.metricAllErrors">metricAllErrors</a></code> | Metric for the number of Errors executing all Lambdas. |
| <code><a href="#cdk-constructs.ThronNewRelicDockerLambda.metricAllInvocations">metricAllInvocations</a></code> | Metric for the number of invocations of all Lambdas. |
| <code><a href="#cdk-constructs.ThronNewRelicDockerLambda.metricAllThrottles">metricAllThrottles</a></code> | Metric for the number of throttled invocations of all Lambdas. |
| <code><a href="#cdk-constructs.ThronNewRelicDockerLambda.metricAllUnreservedConcurrentExecutions">metricAllUnreservedConcurrentExecutions</a></code> | Metric for the number of unreserved concurrent executions across all Lambdas. |

---

##### `isConstruct` <a name="isConstruct" id="cdk-constructs.ThronNewRelicDockerLambda.isConstruct"></a>

```typescript
import { ThronNewRelicDockerLambda } from 'cdk-constructs'

ThronNewRelicDockerLambda.isConstruct(x: any)
```

Checks if `x` is a construct.

Use this method instead of `instanceof` to properly detect `Construct`
instances, even when the construct library is symlinked.

Explanation: in JavaScript, multiple copies of the `constructs` library on
disk are seen as independent, completely different libraries. As a
consequence, the class `Construct` in each copy of the `constructs` library
is seen as a different class, and an instance of one class will not test as
`instanceof` the other class. `npm install` will not create installations
like this, but users may manually symlink construct libraries together or
use a monorepo tool: in those cases, multiple copies of the `constructs`
library can be accidentally installed, and `instanceof` will behave
unpredictably. It is safest to avoid using `instanceof`, and using
this type-testing method instead.

###### `x`<sup>Required</sup> <a name="x" id="cdk-constructs.ThronNewRelicDockerLambda.isConstruct.parameter.x"></a>

- *Type:* any

Any object.

---

##### `isOwnedResource` <a name="isOwnedResource" id="cdk-constructs.ThronNewRelicDockerLambda.isOwnedResource"></a>

```typescript
import { ThronNewRelicDockerLambda } from 'cdk-constructs'

ThronNewRelicDockerLambda.isOwnedResource(construct: IConstruct)
```

Returns true if the construct was created by CDK, and false otherwise.

###### `construct`<sup>Required</sup> <a name="construct" id="cdk-constructs.ThronNewRelicDockerLambda.isOwnedResource.parameter.construct"></a>

- *Type:* constructs.IConstruct

---

##### `isResource` <a name="isResource" id="cdk-constructs.ThronNewRelicDockerLambda.isResource"></a>

```typescript
import { ThronNewRelicDockerLambda } from 'cdk-constructs'

ThronNewRelicDockerLambda.isResource(construct: IConstruct)
```

Check whether the given construct is a Resource.

###### `construct`<sup>Required</sup> <a name="construct" id="cdk-constructs.ThronNewRelicDockerLambda.isResource.parameter.construct"></a>

- *Type:* constructs.IConstruct

---

##### `classifyVersionProperty` <a name="classifyVersionProperty" id="cdk-constructs.ThronNewRelicDockerLambda.classifyVersionProperty"></a>

```typescript
import { ThronNewRelicDockerLambda } from 'cdk-constructs'

ThronNewRelicDockerLambda.classifyVersionProperty(propertyName: string, locked: boolean)
```

Record whether specific properties in the `AWS::Lambda::Function` resource should also be associated to the Version resource.

See 'currentVersion' section in the module README for more details.

###### `propertyName`<sup>Required</sup> <a name="propertyName" id="cdk-constructs.ThronNewRelicDockerLambda.classifyVersionProperty.parameter.propertyName"></a>

- *Type:* string

The property to classify.

---

###### `locked`<sup>Required</sup> <a name="locked" id="cdk-constructs.ThronNewRelicDockerLambda.classifyVersionProperty.parameter.locked"></a>

- *Type:* boolean

whether the property should be associated to the version or not.

---

##### `fromFunctionArn` <a name="fromFunctionArn" id="cdk-constructs.ThronNewRelicDockerLambda.fromFunctionArn"></a>

```typescript
import { ThronNewRelicDockerLambda } from 'cdk-constructs'

ThronNewRelicDockerLambda.fromFunctionArn(scope: Construct, id: string, functionArn: string)
```

Import a lambda function into the CDK using its ARN.

For `Function.addPermissions()` to work on this imported lambda, make sure that is
in the same account and region as the stack you are importing it into.

###### `scope`<sup>Required</sup> <a name="scope" id="cdk-constructs.ThronNewRelicDockerLambda.fromFunctionArn.parameter.scope"></a>

- *Type:* constructs.Construct

---

###### `id`<sup>Required</sup> <a name="id" id="cdk-constructs.ThronNewRelicDockerLambda.fromFunctionArn.parameter.id"></a>

- *Type:* string

---

###### `functionArn`<sup>Required</sup> <a name="functionArn" id="cdk-constructs.ThronNewRelicDockerLambda.fromFunctionArn.parameter.functionArn"></a>

- *Type:* string

---

##### `fromFunctionAttributes` <a name="fromFunctionAttributes" id="cdk-constructs.ThronNewRelicDockerLambda.fromFunctionAttributes"></a>

```typescript
import { ThronNewRelicDockerLambda } from 'cdk-constructs'

ThronNewRelicDockerLambda.fromFunctionAttributes(scope: Construct, id: string, attrs: FunctionAttributes)
```

Creates a Lambda function object which represents a function not defined within this stack.

For `Function.addPermissions()` to work on this imported lambda, set the sameEnvironment property to true
if this imported lambda is in the same account and region as the stack you are importing it into.

###### `scope`<sup>Required</sup> <a name="scope" id="cdk-constructs.ThronNewRelicDockerLambda.fromFunctionAttributes.parameter.scope"></a>

- *Type:* constructs.Construct

The parent construct.

---

###### `id`<sup>Required</sup> <a name="id" id="cdk-constructs.ThronNewRelicDockerLambda.fromFunctionAttributes.parameter.id"></a>

- *Type:* string

The name of the lambda construct.

---

###### `attrs`<sup>Required</sup> <a name="attrs" id="cdk-constructs.ThronNewRelicDockerLambda.fromFunctionAttributes.parameter.attrs"></a>

- *Type:* aws-cdk-lib.aws_lambda.FunctionAttributes

the attributes of the function to import.

---

##### `fromFunctionName` <a name="fromFunctionName" id="cdk-constructs.ThronNewRelicDockerLambda.fromFunctionName"></a>

```typescript
import { ThronNewRelicDockerLambda } from 'cdk-constructs'

ThronNewRelicDockerLambda.fromFunctionName(scope: Construct, id: string, functionName: string)
```

Import a lambda function into the CDK using its name.

###### `scope`<sup>Required</sup> <a name="scope" id="cdk-constructs.ThronNewRelicDockerLambda.fromFunctionName.parameter.scope"></a>

- *Type:* constructs.Construct

---

###### `id`<sup>Required</sup> <a name="id" id="cdk-constructs.ThronNewRelicDockerLambda.fromFunctionName.parameter.id"></a>

- *Type:* string

---

###### `functionName`<sup>Required</sup> <a name="functionName" id="cdk-constructs.ThronNewRelicDockerLambda.fromFunctionName.parameter.functionName"></a>

- *Type:* string

---

##### `metricAll` <a name="metricAll" id="cdk-constructs.ThronNewRelicDockerLambda.metricAll"></a>

```typescript
import { ThronNewRelicDockerLambda } from 'cdk-constructs'

ThronNewRelicDockerLambda.metricAll(metricName: string, props?: MetricOptions)
```

Return the given named metric for this Lambda.

###### `metricName`<sup>Required</sup> <a name="metricName" id="cdk-constructs.ThronNewRelicDockerLambda.metricAll.parameter.metricName"></a>

- *Type:* string

---

###### `props`<sup>Optional</sup> <a name="props" id="cdk-constructs.ThronNewRelicDockerLambda.metricAll.parameter.props"></a>

- *Type:* aws-cdk-lib.aws_cloudwatch.MetricOptions

---

##### `metricAllConcurrentExecutions` <a name="metricAllConcurrentExecutions" id="cdk-constructs.ThronNewRelicDockerLambda.metricAllConcurrentExecutions"></a>

```typescript
import { ThronNewRelicDockerLambda } from 'cdk-constructs'

ThronNewRelicDockerLambda.metricAllConcurrentExecutions(props?: MetricOptions)
```

Metric for the number of concurrent executions across all Lambdas.

###### `props`<sup>Optional</sup> <a name="props" id="cdk-constructs.ThronNewRelicDockerLambda.metricAllConcurrentExecutions.parameter.props"></a>

- *Type:* aws-cdk-lib.aws_cloudwatch.MetricOptions

---

##### `metricAllDuration` <a name="metricAllDuration" id="cdk-constructs.ThronNewRelicDockerLambda.metricAllDuration"></a>

```typescript
import { ThronNewRelicDockerLambda } from 'cdk-constructs'

ThronNewRelicDockerLambda.metricAllDuration(props?: MetricOptions)
```

Metric for the Duration executing all Lambdas.

###### `props`<sup>Optional</sup> <a name="props" id="cdk-constructs.ThronNewRelicDockerLambda.metricAllDuration.parameter.props"></a>

- *Type:* aws-cdk-lib.aws_cloudwatch.MetricOptions

---

##### `metricAllErrors` <a name="metricAllErrors" id="cdk-constructs.ThronNewRelicDockerLambda.metricAllErrors"></a>

```typescript
import { ThronNewRelicDockerLambda } from 'cdk-constructs'

ThronNewRelicDockerLambda.metricAllErrors(props?: MetricOptions)
```

Metric for the number of Errors executing all Lambdas.

###### `props`<sup>Optional</sup> <a name="props" id="cdk-constructs.ThronNewRelicDockerLambda.metricAllErrors.parameter.props"></a>

- *Type:* aws-cdk-lib.aws_cloudwatch.MetricOptions

---

##### `metricAllInvocations` <a name="metricAllInvocations" id="cdk-constructs.ThronNewRelicDockerLambda.metricAllInvocations"></a>

```typescript
import { ThronNewRelicDockerLambda } from 'cdk-constructs'

ThronNewRelicDockerLambda.metricAllInvocations(props?: MetricOptions)
```

Metric for the number of invocations of all Lambdas.

###### `props`<sup>Optional</sup> <a name="props" id="cdk-constructs.ThronNewRelicDockerLambda.metricAllInvocations.parameter.props"></a>

- *Type:* aws-cdk-lib.aws_cloudwatch.MetricOptions

---

##### `metricAllThrottles` <a name="metricAllThrottles" id="cdk-constructs.ThronNewRelicDockerLambda.metricAllThrottles"></a>

```typescript
import { ThronNewRelicDockerLambda } from 'cdk-constructs'

ThronNewRelicDockerLambda.metricAllThrottles(props?: MetricOptions)
```

Metric for the number of throttled invocations of all Lambdas.

###### `props`<sup>Optional</sup> <a name="props" id="cdk-constructs.ThronNewRelicDockerLambda.metricAllThrottles.parameter.props"></a>

- *Type:* aws-cdk-lib.aws_cloudwatch.MetricOptions

---

##### `metricAllUnreservedConcurrentExecutions` <a name="metricAllUnreservedConcurrentExecutions" id="cdk-constructs.ThronNewRelicDockerLambda.metricAllUnreservedConcurrentExecutions"></a>

```typescript
import { ThronNewRelicDockerLambda } from 'cdk-constructs'

ThronNewRelicDockerLambda.metricAllUnreservedConcurrentExecutions(props?: MetricOptions)
```

Metric for the number of unreserved concurrent executions across all Lambdas.

###### `props`<sup>Optional</sup> <a name="props" id="cdk-constructs.ThronNewRelicDockerLambda.metricAllUnreservedConcurrentExecutions.parameter.props"></a>

- *Type:* aws-cdk-lib.aws_cloudwatch.MetricOptions

---

#### Properties <a name="Properties" id="Properties"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.ThronNewRelicDockerLambda.property.node">node</a></code> | <code>constructs.Node</code> | The tree node. |
| <code><a href="#cdk-constructs.ThronNewRelicDockerLambda.property.env">env</a></code> | <code>aws-cdk-lib.ResourceEnvironment</code> | The environment this resource belongs to. |
| <code><a href="#cdk-constructs.ThronNewRelicDockerLambda.property.stack">stack</a></code> | <code>aws-cdk-lib.Stack</code> | The stack in which this resource is defined. |
| <code><a href="#cdk-constructs.ThronNewRelicDockerLambda.property.architecture">architecture</a></code> | <code>aws-cdk-lib.aws_lambda.Architecture</code> | The architecture of this Lambda Function (this is an optional attribute and defaults to X86_64). |
| <code><a href="#cdk-constructs.ThronNewRelicDockerLambda.property.connections">connections</a></code> | <code>aws-cdk-lib.aws_ec2.Connections</code> | Access the Connections object. |
| <code><a href="#cdk-constructs.ThronNewRelicDockerLambda.property.functionArn">functionArn</a></code> | <code>string</code> | ARN of this function. |
| <code><a href="#cdk-constructs.ThronNewRelicDockerLambda.property.functionName">functionName</a></code> | <code>string</code> | Name of this function. |
| <code><a href="#cdk-constructs.ThronNewRelicDockerLambda.property.grantPrincipal">grantPrincipal</a></code> | <code>aws-cdk-lib.aws_iam.IPrincipal</code> | The principal this Lambda Function is running as. |
| <code><a href="#cdk-constructs.ThronNewRelicDockerLambda.property.isBoundToVpc">isBoundToVpc</a></code> | <code>boolean</code> | Whether or not this Lambda function was bound to a VPC. |
| <code><a href="#cdk-constructs.ThronNewRelicDockerLambda.property.latestVersion">latestVersion</a></code> | <code>aws-cdk-lib.aws_lambda.IVersion</code> | The `$LATEST` version of this function. |
| <code><a href="#cdk-constructs.ThronNewRelicDockerLambda.property.permissionsNode">permissionsNode</a></code> | <code>constructs.Node</code> | The construct node where permissions are attached. |
| <code><a href="#cdk-constructs.ThronNewRelicDockerLambda.property.resourceArnsForGrantInvoke">resourceArnsForGrantInvoke</a></code> | <code>string[]</code> | The ARN(s) to put into the resource field of the generated IAM policy for grantInvoke(). |
| <code><a href="#cdk-constructs.ThronNewRelicDockerLambda.property.role">role</a></code> | <code>aws-cdk-lib.aws_iam.IRole</code> | Execution role associated with this function. |
| <code><a href="#cdk-constructs.ThronNewRelicDockerLambda.property.currentVersion">currentVersion</a></code> | <code>aws-cdk-lib.aws_lambda.Version</code> | Returns a `lambda.Version` which represents the current version of this Lambda function. A new version will be created every time the function's configuration changes. |
| <code><a href="#cdk-constructs.ThronNewRelicDockerLambda.property.logGroup">logGroup</a></code> | <code>aws-cdk-lib.aws_logs.ILogGroup</code> | The LogGroup where the Lambda function's logs are made available. |
| <code><a href="#cdk-constructs.ThronNewRelicDockerLambda.property.runtime">runtime</a></code> | <code>aws-cdk-lib.aws_lambda.Runtime</code> | The runtime configured for this lambda. |
| <code><a href="#cdk-constructs.ThronNewRelicDockerLambda.property.deadLetterQueue">deadLetterQueue</a></code> | <code>aws-cdk-lib.aws_sqs.IQueue</code> | The DLQ (as queue) associated with this Lambda Function (this is an optional attribute). |
| <code><a href="#cdk-constructs.ThronNewRelicDockerLambda.property.deadLetterTopic">deadLetterTopic</a></code> | <code>aws-cdk-lib.aws_sns.ITopic</code> | The DLQ (as topic) associated with this Lambda Function (this is an optional attribute). |
| <code><a href="#cdk-constructs.ThronNewRelicDockerLambda.property.timeout">timeout</a></code> | <code>aws-cdk-lib.Duration</code> | The timeout configured for this lambda. |
| <code><a href="#cdk-constructs.ThronNewRelicDockerLambda.property.apiGatewayEndpoints">apiGatewayEndpoints</a></code> | <code>{[ key: string ]: <a href="#cdk-constructs.ThronCreatedApiGatewayEndpoint">ThronCreatedApiGatewayEndpoint</a>}</code> | *No description.* |
| <code><a href="#cdk-constructs.ThronNewRelicDockerLambda.property.endpoints">endpoints</a></code> | <code>{[ key: string ]: <a href="#cdk-constructs.EndpointAlb">EndpointAlb</a>}</code> | *No description.* |
| <code><a href="#cdk-constructs.ThronNewRelicDockerLambda.property.legacyEndpoints">legacyEndpoints</a></code> | <code>{[ key: string ]: <a href="#cdk-constructs.EndpointAlb">EndpointAlb</a>}</code> | *No description.* |

---

##### `node`<sup>Required</sup> <a name="node" id="cdk-constructs.ThronNewRelicDockerLambda.property.node"></a>

```typescript
public readonly node: Node;
```

- *Type:* constructs.Node

The tree node.

---

##### `env`<sup>Required</sup> <a name="env" id="cdk-constructs.ThronNewRelicDockerLambda.property.env"></a>

```typescript
public readonly env: ResourceEnvironment;
```

- *Type:* aws-cdk-lib.ResourceEnvironment

The environment this resource belongs to.

For resources that are created and managed by the CDK
(generally, those created by creating new class instances like Role, Bucket, etc.),
this is always the same as the environment of the stack they belong to;
however, for imported resources
(those obtained from static methods like fromRoleArn, fromBucketName, etc.),
that might be different than the stack they were imported into.

---

##### `stack`<sup>Required</sup> <a name="stack" id="cdk-constructs.ThronNewRelicDockerLambda.property.stack"></a>

```typescript
public readonly stack: Stack;
```

- *Type:* aws-cdk-lib.Stack

The stack in which this resource is defined.

---

##### `architecture`<sup>Required</sup> <a name="architecture" id="cdk-constructs.ThronNewRelicDockerLambda.property.architecture"></a>

```typescript
public readonly architecture: Architecture;
```

- *Type:* aws-cdk-lib.aws_lambda.Architecture

The architecture of this Lambda Function (this is an optional attribute and defaults to X86_64).

---

##### `connections`<sup>Required</sup> <a name="connections" id="cdk-constructs.ThronNewRelicDockerLambda.property.connections"></a>

```typescript
public readonly connections: Connections;
```

- *Type:* aws-cdk-lib.aws_ec2.Connections

Access the Connections object.

Will fail if not a VPC-enabled Lambda Function

---

##### `functionArn`<sup>Required</sup> <a name="functionArn" id="cdk-constructs.ThronNewRelicDockerLambda.property.functionArn"></a>

```typescript
public readonly functionArn: string;
```

- *Type:* string

ARN of this function.

---

##### `functionName`<sup>Required</sup> <a name="functionName" id="cdk-constructs.ThronNewRelicDockerLambda.property.functionName"></a>

```typescript
public readonly functionName: string;
```

- *Type:* string

Name of this function.

---

##### `grantPrincipal`<sup>Required</sup> <a name="grantPrincipal" id="cdk-constructs.ThronNewRelicDockerLambda.property.grantPrincipal"></a>

```typescript
public readonly grantPrincipal: IPrincipal;
```

- *Type:* aws-cdk-lib.aws_iam.IPrincipal

The principal this Lambda Function is running as.

---

##### `isBoundToVpc`<sup>Required</sup> <a name="isBoundToVpc" id="cdk-constructs.ThronNewRelicDockerLambda.property.isBoundToVpc"></a>

```typescript
public readonly isBoundToVpc: boolean;
```

- *Type:* boolean

Whether or not this Lambda function was bound to a VPC.

If this is is `false`, trying to access the `connections` object will fail.

---

##### `latestVersion`<sup>Required</sup> <a name="latestVersion" id="cdk-constructs.ThronNewRelicDockerLambda.property.latestVersion"></a>

```typescript
public readonly latestVersion: IVersion;
```

- *Type:* aws-cdk-lib.aws_lambda.IVersion

The `$LATEST` version of this function.

Note that this is reference to a non-specific AWS Lambda version, which
means the function this version refers to can return different results in
different invocations.

To obtain a reference to an explicit version which references the current
function configuration, use `lambdaFunction.currentVersion` instead.

---

##### `permissionsNode`<sup>Required</sup> <a name="permissionsNode" id="cdk-constructs.ThronNewRelicDockerLambda.property.permissionsNode"></a>

```typescript
public readonly permissionsNode: Node;
```

- *Type:* constructs.Node

The construct node where permissions are attached.

---

##### `resourceArnsForGrantInvoke`<sup>Required</sup> <a name="resourceArnsForGrantInvoke" id="cdk-constructs.ThronNewRelicDockerLambda.property.resourceArnsForGrantInvoke"></a>

```typescript
public readonly resourceArnsForGrantInvoke: string[];
```

- *Type:* string[]

The ARN(s) to put into the resource field of the generated IAM policy for grantInvoke().

---

##### `role`<sup>Optional</sup> <a name="role" id="cdk-constructs.ThronNewRelicDockerLambda.property.role"></a>

```typescript
public readonly role: IRole;
```

- *Type:* aws-cdk-lib.aws_iam.IRole

Execution role associated with this function.

---

##### `currentVersion`<sup>Required</sup> <a name="currentVersion" id="cdk-constructs.ThronNewRelicDockerLambda.property.currentVersion"></a>

```typescript
public readonly currentVersion: Version;
```

- *Type:* aws-cdk-lib.aws_lambda.Version

Returns a `lambda.Version` which represents the current version of this Lambda function. A new version will be created every time the function's configuration changes.

You can specify options for this version using the `currentVersionOptions`
prop when initializing the `lambda.Function`.

---

##### `logGroup`<sup>Required</sup> <a name="logGroup" id="cdk-constructs.ThronNewRelicDockerLambda.property.logGroup"></a>

```typescript
public readonly logGroup: ILogGroup;
```

- *Type:* aws-cdk-lib.aws_logs.ILogGroup

The LogGroup where the Lambda function's logs are made available.

If either `logRetention` is set or this property is called, a CloudFormation custom resource is added to the stack that
pre-creates the log group as part of the stack deployment, if it already doesn't exist, and sets the correct log retention
period (never expire, by default).

Further, if the log group already exists and the `logRetention` is not set, the custom resource will reset the log retention
to never expire even if it was configured with a different value.

---

##### `runtime`<sup>Required</sup> <a name="runtime" id="cdk-constructs.ThronNewRelicDockerLambda.property.runtime"></a>

```typescript
public readonly runtime: Runtime;
```

- *Type:* aws-cdk-lib.aws_lambda.Runtime

The runtime configured for this lambda.

---

##### `deadLetterQueue`<sup>Optional</sup> <a name="deadLetterQueue" id="cdk-constructs.ThronNewRelicDockerLambda.property.deadLetterQueue"></a>

```typescript
public readonly deadLetterQueue: IQueue;
```

- *Type:* aws-cdk-lib.aws_sqs.IQueue

The DLQ (as queue) associated with this Lambda Function (this is an optional attribute).

---

##### `deadLetterTopic`<sup>Optional</sup> <a name="deadLetterTopic" id="cdk-constructs.ThronNewRelicDockerLambda.property.deadLetterTopic"></a>

```typescript
public readonly deadLetterTopic: ITopic;
```

- *Type:* aws-cdk-lib.aws_sns.ITopic

The DLQ (as topic) associated with this Lambda Function (this is an optional attribute).

---

##### `timeout`<sup>Optional</sup> <a name="timeout" id="cdk-constructs.ThronNewRelicDockerLambda.property.timeout"></a>

```typescript
public readonly timeout: Duration;
```

- *Type:* aws-cdk-lib.Duration

The timeout configured for this lambda.

---

##### `apiGatewayEndpoints`<sup>Optional</sup> <a name="apiGatewayEndpoints" id="cdk-constructs.ThronNewRelicDockerLambda.property.apiGatewayEndpoints"></a>

```typescript
public readonly apiGatewayEndpoints: {[ key: string ]: ThronCreatedApiGatewayEndpoint};
```

- *Type:* {[ key: string ]: <a href="#cdk-constructs.ThronCreatedApiGatewayEndpoint">ThronCreatedApiGatewayEndpoint</a>}

---

##### `endpoints`<sup>Optional</sup> <a name="endpoints" id="cdk-constructs.ThronNewRelicDockerLambda.property.endpoints"></a>

```typescript
public readonly endpoints: {[ key: string ]: EndpointAlb};
```

- *Type:* {[ key: string ]: <a href="#cdk-constructs.EndpointAlb">EndpointAlb</a>}

---

##### `legacyEndpoints`<sup>Optional</sup> <a name="legacyEndpoints" id="cdk-constructs.ThronNewRelicDockerLambda.property.legacyEndpoints"></a>

```typescript
public readonly legacyEndpoints: {[ key: string ]: EndpointAlb};
```

- *Type:* {[ key: string ]: <a href="#cdk-constructs.EndpointAlb">EndpointAlb</a>}

---


### ThronPipelineBuildProject <a name="ThronPipelineBuildProject" id="cdk-constructs.ThronPipelineBuildProject"></a>

- *Implements:* aws-cdk-lib.aws_iam.IGrantable

#### Initializers <a name="Initializers" id="cdk-constructs.ThronPipelineBuildProject.Initializer"></a>

```typescript
import { ThronPipelineBuildProject } from 'cdk-constructs'

new ThronPipelineBuildProject(scope: Construct, id: string, props: ThronPipelineBuildProjectProps)
```

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.ThronPipelineBuildProject.Initializer.parameter.scope">scope</a></code> | <code>constructs.Construct</code> | *No description.* |
| <code><a href="#cdk-constructs.ThronPipelineBuildProject.Initializer.parameter.id">id</a></code> | <code>string</code> | *No description.* |
| <code><a href="#cdk-constructs.ThronPipelineBuildProject.Initializer.parameter.props">props</a></code> | <code><a href="#cdk-constructs.ThronPipelineBuildProjectProps">ThronPipelineBuildProjectProps</a></code> | *No description.* |

---

##### `scope`<sup>Required</sup> <a name="scope" id="cdk-constructs.ThronPipelineBuildProject.Initializer.parameter.scope"></a>

- *Type:* constructs.Construct

---

##### `id`<sup>Required</sup> <a name="id" id="cdk-constructs.ThronPipelineBuildProject.Initializer.parameter.id"></a>

- *Type:* string

---

##### `props`<sup>Required</sup> <a name="props" id="cdk-constructs.ThronPipelineBuildProject.Initializer.parameter.props"></a>

- *Type:* <a href="#cdk-constructs.ThronPipelineBuildProjectProps">ThronPipelineBuildProjectProps</a>

---

#### Methods <a name="Methods" id="Methods"></a>

| **Name** | **Description** |
| --- | --- |
| <code><a href="#cdk-constructs.ThronPipelineBuildProject.toString">toString</a></code> | Returns a string representation of this construct. |
| <code><a href="#cdk-constructs.ThronPipelineBuildProject.allowCDKAccessToAccount">allowCDKAccessToAccount</a></code> | *No description.* |
| <code><a href="#cdk-constructs.ThronPipelineBuildProject.allowEcrForRepo">allowEcrForRepo</a></code> | *No description.* |

---

##### `toString` <a name="toString" id="cdk-constructs.ThronPipelineBuildProject.toString"></a>

```typescript
public toString(): string
```

Returns a string representation of this construct.

##### `allowCDKAccessToAccount` <a name="allowCDKAccessToAccount" id="cdk-constructs.ThronPipelineBuildProject.allowCDKAccessToAccount"></a>

```typescript
public allowCDKAccessToAccount(accountId: string): void
```

###### `accountId`<sup>Required</sup> <a name="accountId" id="cdk-constructs.ThronPipelineBuildProject.allowCDKAccessToAccount.parameter.accountId"></a>

- *Type:* string

---

##### `allowEcrForRepo` <a name="allowEcrForRepo" id="cdk-constructs.ThronPipelineBuildProject.allowEcrForRepo"></a>

```typescript
public allowEcrForRepo(ecrRepository: Repository): void
```

###### `ecrRepository`<sup>Required</sup> <a name="ecrRepository" id="cdk-constructs.ThronPipelineBuildProject.allowEcrForRepo.parameter.ecrRepository"></a>

- *Type:* aws-cdk-lib.aws_ecr.Repository

---

#### Static Functions <a name="Static Functions" id="Static Functions"></a>

| **Name** | **Description** |
| --- | --- |
| <code><a href="#cdk-constructs.ThronPipelineBuildProject.isConstruct">isConstruct</a></code> | Checks if `x` is a construct. |

---

##### `isConstruct` <a name="isConstruct" id="cdk-constructs.ThronPipelineBuildProject.isConstruct"></a>

```typescript
import { ThronPipelineBuildProject } from 'cdk-constructs'

ThronPipelineBuildProject.isConstruct(x: any)
```

Checks if `x` is a construct.

Use this method instead of `instanceof` to properly detect `Construct`
instances, even when the construct library is symlinked.

Explanation: in JavaScript, multiple copies of the `constructs` library on
disk are seen as independent, completely different libraries. As a
consequence, the class `Construct` in each copy of the `constructs` library
is seen as a different class, and an instance of one class will not test as
`instanceof` the other class. `npm install` will not create installations
like this, but users may manually symlink construct libraries together or
use a monorepo tool: in those cases, multiple copies of the `constructs`
library can be accidentally installed, and `instanceof` will behave
unpredictably. It is safest to avoid using `instanceof`, and using
this type-testing method instead.

###### `x`<sup>Required</sup> <a name="x" id="cdk-constructs.ThronPipelineBuildProject.isConstruct.parameter.x"></a>

- *Type:* any

Any object.

---

#### Properties <a name="Properties" id="Properties"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.ThronPipelineBuildProject.property.node">node</a></code> | <code>constructs.Node</code> | The tree node. |
| <code><a href="#cdk-constructs.ThronPipelineBuildProject.property.grantPrincipal">grantPrincipal</a></code> | <code>aws-cdk-lib.aws_iam.IPrincipal</code> | The principal to grant permissions to. |
| <code><a href="#cdk-constructs.ThronPipelineBuildProject.property.buildName">buildName</a></code> | <code>string</code> | *No description.* |
| <code><a href="#cdk-constructs.ThronPipelineBuildProject.property.project">project</a></code> | <code>aws-cdk-lib.aws_codebuild.Project</code> | *No description.* |
| <code><a href="#cdk-constructs.ThronPipelineBuildProject.property.role">role</a></code> | <code>aws-cdk-lib.aws_iam.Role</code> | *No description.* |

---

##### `node`<sup>Required</sup> <a name="node" id="cdk-constructs.ThronPipelineBuildProject.property.node"></a>

```typescript
public readonly node: Node;
```

- *Type:* constructs.Node

The tree node.

---

##### `grantPrincipal`<sup>Required</sup> <a name="grantPrincipal" id="cdk-constructs.ThronPipelineBuildProject.property.grantPrincipal"></a>

```typescript
public readonly grantPrincipal: IPrincipal;
```

- *Type:* aws-cdk-lib.aws_iam.IPrincipal

The principal to grant permissions to.

---

##### `buildName`<sup>Required</sup> <a name="buildName" id="cdk-constructs.ThronPipelineBuildProject.property.buildName"></a>

```typescript
public readonly buildName: string;
```

- *Type:* string

---

##### `project`<sup>Required</sup> <a name="project" id="cdk-constructs.ThronPipelineBuildProject.property.project"></a>

```typescript
public readonly project: Project;
```

- *Type:* aws-cdk-lib.aws_codebuild.Project

---

##### `role`<sup>Required</sup> <a name="role" id="cdk-constructs.ThronPipelineBuildProject.property.role"></a>

```typescript
public readonly role: Role;
```

- *Type:* aws-cdk-lib.aws_iam.Role

---


### ThronResponseHeaderPolicy <a name="ThronResponseHeaderPolicy" id="cdk-constructs.ThronResponseHeaderPolicy"></a>

#### Initializers <a name="Initializers" id="cdk-constructs.ThronResponseHeaderPolicy.Initializer"></a>

```typescript
import { ThronResponseHeaderPolicy } from 'cdk-constructs'

new ThronResponseHeaderPolicy(scope: Construct, id: string, props?: ResponseHeadersPolicyProps)
```

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.ThronResponseHeaderPolicy.Initializer.parameter.scope">scope</a></code> | <code>constructs.Construct</code> | *No description.* |
| <code><a href="#cdk-constructs.ThronResponseHeaderPolicy.Initializer.parameter.id">id</a></code> | <code>string</code> | *No description.* |
| <code><a href="#cdk-constructs.ThronResponseHeaderPolicy.Initializer.parameter.props">props</a></code> | <code>aws-cdk-lib.aws_cloudfront.ResponseHeadersPolicyProps</code> | *No description.* |

---

##### `scope`<sup>Required</sup> <a name="scope" id="cdk-constructs.ThronResponseHeaderPolicy.Initializer.parameter.scope"></a>

- *Type:* constructs.Construct

---

##### `id`<sup>Required</sup> <a name="id" id="cdk-constructs.ThronResponseHeaderPolicy.Initializer.parameter.id"></a>

- *Type:* string

---

##### `props`<sup>Optional</sup> <a name="props" id="cdk-constructs.ThronResponseHeaderPolicy.Initializer.parameter.props"></a>

- *Type:* aws-cdk-lib.aws_cloudfront.ResponseHeadersPolicyProps

---

#### Methods <a name="Methods" id="Methods"></a>

| **Name** | **Description** |
| --- | --- |
| <code><a href="#cdk-constructs.ThronResponseHeaderPolicy.toString">toString</a></code> | Returns a string representation of this construct. |
| <code><a href="#cdk-constructs.ThronResponseHeaderPolicy.applyRemovalPolicy">applyRemovalPolicy</a></code> | Apply the given removal policy to this resource. |

---

##### `toString` <a name="toString" id="cdk-constructs.ThronResponseHeaderPolicy.toString"></a>

```typescript
public toString(): string
```

Returns a string representation of this construct.

##### `applyRemovalPolicy` <a name="applyRemovalPolicy" id="cdk-constructs.ThronResponseHeaderPolicy.applyRemovalPolicy"></a>

```typescript
public applyRemovalPolicy(policy: RemovalPolicy): void
```

Apply the given removal policy to this resource.

The Removal Policy controls what happens to this resource when it stops
being managed by CloudFormation, either because you've removed it from the
CDK application or because you've made a change that requires the resource
to be replaced.

The resource can be deleted (`RemovalPolicy.DESTROY`), or left in your AWS
account for data recovery and cleanup later (`RemovalPolicy.RETAIN`).

###### `policy`<sup>Required</sup> <a name="policy" id="cdk-constructs.ThronResponseHeaderPolicy.applyRemovalPolicy.parameter.policy"></a>

- *Type:* aws-cdk-lib.RemovalPolicy

---

#### Static Functions <a name="Static Functions" id="Static Functions"></a>

| **Name** | **Description** |
| --- | --- |
| <code><a href="#cdk-constructs.ThronResponseHeaderPolicy.isConstruct">isConstruct</a></code> | Checks if `x` is a construct. |
| <code><a href="#cdk-constructs.ThronResponseHeaderPolicy.isOwnedResource">isOwnedResource</a></code> | Returns true if the construct was created by CDK, and false otherwise. |
| <code><a href="#cdk-constructs.ThronResponseHeaderPolicy.isResource">isResource</a></code> | Check whether the given construct is a Resource. |
| <code><a href="#cdk-constructs.ThronResponseHeaderPolicy.fromResponseHeadersPolicyId">fromResponseHeadersPolicyId</a></code> | Import an existing Response Headers Policy from its ID. |
| <code><a href="#cdk-constructs.ThronResponseHeaderPolicy.default">default</a></code> | Generates a `ThronResponseHeaderPolicy` with all the default values. |
| <code><a href="#cdk-constructs.ThronResponseHeaderPolicy.defaultWithOverrides">defaultWithOverrides</a></code> | Generates a `ThronResponseHeaderPolicy` with all the default values except for the ones passed on `props`. |

---

##### `isConstruct` <a name="isConstruct" id="cdk-constructs.ThronResponseHeaderPolicy.isConstruct"></a>

```typescript
import { ThronResponseHeaderPolicy } from 'cdk-constructs'

ThronResponseHeaderPolicy.isConstruct(x: any)
```

Checks if `x` is a construct.

Use this method instead of `instanceof` to properly detect `Construct`
instances, even when the construct library is symlinked.

Explanation: in JavaScript, multiple copies of the `constructs` library on
disk are seen as independent, completely different libraries. As a
consequence, the class `Construct` in each copy of the `constructs` library
is seen as a different class, and an instance of one class will not test as
`instanceof` the other class. `npm install` will not create installations
like this, but users may manually symlink construct libraries together or
use a monorepo tool: in those cases, multiple copies of the `constructs`
library can be accidentally installed, and `instanceof` will behave
unpredictably. It is safest to avoid using `instanceof`, and using
this type-testing method instead.

###### `x`<sup>Required</sup> <a name="x" id="cdk-constructs.ThronResponseHeaderPolicy.isConstruct.parameter.x"></a>

- *Type:* any

Any object.

---

##### `isOwnedResource` <a name="isOwnedResource" id="cdk-constructs.ThronResponseHeaderPolicy.isOwnedResource"></a>

```typescript
import { ThronResponseHeaderPolicy } from 'cdk-constructs'

ThronResponseHeaderPolicy.isOwnedResource(construct: IConstruct)
```

Returns true if the construct was created by CDK, and false otherwise.

###### `construct`<sup>Required</sup> <a name="construct" id="cdk-constructs.ThronResponseHeaderPolicy.isOwnedResource.parameter.construct"></a>

- *Type:* constructs.IConstruct

---

##### `isResource` <a name="isResource" id="cdk-constructs.ThronResponseHeaderPolicy.isResource"></a>

```typescript
import { ThronResponseHeaderPolicy } from 'cdk-constructs'

ThronResponseHeaderPolicy.isResource(construct: IConstruct)
```

Check whether the given construct is a Resource.

###### `construct`<sup>Required</sup> <a name="construct" id="cdk-constructs.ThronResponseHeaderPolicy.isResource.parameter.construct"></a>

- *Type:* constructs.IConstruct

---

##### `fromResponseHeadersPolicyId` <a name="fromResponseHeadersPolicyId" id="cdk-constructs.ThronResponseHeaderPolicy.fromResponseHeadersPolicyId"></a>

```typescript
import { ThronResponseHeaderPolicy } from 'cdk-constructs'

ThronResponseHeaderPolicy.fromResponseHeadersPolicyId(scope: Construct, id: string, responseHeadersPolicyId: string)
```

Import an existing Response Headers Policy from its ID.

###### `scope`<sup>Required</sup> <a name="scope" id="cdk-constructs.ThronResponseHeaderPolicy.fromResponseHeadersPolicyId.parameter.scope"></a>

- *Type:* constructs.Construct

---

###### `id`<sup>Required</sup> <a name="id" id="cdk-constructs.ThronResponseHeaderPolicy.fromResponseHeadersPolicyId.parameter.id"></a>

- *Type:* string

---

###### `responseHeadersPolicyId`<sup>Required</sup> <a name="responseHeadersPolicyId" id="cdk-constructs.ThronResponseHeaderPolicy.fromResponseHeadersPolicyId.parameter.responseHeadersPolicyId"></a>

- *Type:* string

---

##### `default` <a name="default" id="cdk-constructs.ThronResponseHeaderPolicy.default"></a>

```typescript
import { ThronResponseHeaderPolicy } from 'cdk-constructs'

ThronResponseHeaderPolicy.default(scope: Construct, id: string)
```

Generates a `ThronResponseHeaderPolicy` with all the default values.

###### `scope`<sup>Required</sup> <a name="scope" id="cdk-constructs.ThronResponseHeaderPolicy.default.parameter.scope"></a>

- *Type:* constructs.Construct

---

###### `id`<sup>Required</sup> <a name="id" id="cdk-constructs.ThronResponseHeaderPolicy.default.parameter.id"></a>

- *Type:* string

---

##### `defaultWithOverrides` <a name="defaultWithOverrides" id="cdk-constructs.ThronResponseHeaderPolicy.defaultWithOverrides"></a>

```typescript
import { ThronResponseHeaderPolicy } from 'cdk-constructs'

ThronResponseHeaderPolicy.defaultWithOverrides(scope: Construct, id: string, props: ThronResponseHeaderPolicyProps)
```

Generates a `ThronResponseHeaderPolicy` with all the default values except for the ones passed on `props`.

###### `scope`<sup>Required</sup> <a name="scope" id="cdk-constructs.ThronResponseHeaderPolicy.defaultWithOverrides.parameter.scope"></a>

- *Type:* constructs.Construct

---

###### `id`<sup>Required</sup> <a name="id" id="cdk-constructs.ThronResponseHeaderPolicy.defaultWithOverrides.parameter.id"></a>

- *Type:* string

---

###### `props`<sup>Required</sup> <a name="props" id="cdk-constructs.ThronResponseHeaderPolicy.defaultWithOverrides.parameter.props"></a>

- *Type:* <a href="#cdk-constructs.ThronResponseHeaderPolicyProps">ThronResponseHeaderPolicyProps</a>

---

#### Properties <a name="Properties" id="Properties"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.ThronResponseHeaderPolicy.property.node">node</a></code> | <code>constructs.Node</code> | The tree node. |
| <code><a href="#cdk-constructs.ThronResponseHeaderPolicy.property.env">env</a></code> | <code>aws-cdk-lib.ResourceEnvironment</code> | The environment this resource belongs to. |
| <code><a href="#cdk-constructs.ThronResponseHeaderPolicy.property.stack">stack</a></code> | <code>aws-cdk-lib.Stack</code> | The stack in which this resource is defined. |
| <code><a href="#cdk-constructs.ThronResponseHeaderPolicy.property.responseHeadersPolicyId">responseHeadersPolicyId</a></code> | <code>string</code> | The ID of the response headers policy. |

---

##### `node`<sup>Required</sup> <a name="node" id="cdk-constructs.ThronResponseHeaderPolicy.property.node"></a>

```typescript
public readonly node: Node;
```

- *Type:* constructs.Node

The tree node.

---

##### `env`<sup>Required</sup> <a name="env" id="cdk-constructs.ThronResponseHeaderPolicy.property.env"></a>

```typescript
public readonly env: ResourceEnvironment;
```

- *Type:* aws-cdk-lib.ResourceEnvironment

The environment this resource belongs to.

For resources that are created and managed by the CDK
(generally, those created by creating new class instances like Role, Bucket, etc.),
this is always the same as the environment of the stack they belong to;
however, for imported resources
(those obtained from static methods like fromRoleArn, fromBucketName, etc.),
that might be different than the stack they were imported into.

---

##### `stack`<sup>Required</sup> <a name="stack" id="cdk-constructs.ThronResponseHeaderPolicy.property.stack"></a>

```typescript
public readonly stack: Stack;
```

- *Type:* aws-cdk-lib.Stack

The stack in which this resource is defined.

---

##### `responseHeadersPolicyId`<sup>Required</sup> <a name="responseHeadersPolicyId" id="cdk-constructs.ThronResponseHeaderPolicy.property.responseHeadersPolicyId"></a>

```typescript
public readonly responseHeadersPolicyId: string;
```

- *Type:* string

The ID of the response headers policy.

---

#### Constants <a name="Constants" id="Constants"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.ThronResponseHeaderPolicy.property.CORS_ALLOW_ALL_ORIGINS">CORS_ALLOW_ALL_ORIGINS</a></code> | <code>aws-cdk-lib.aws_cloudfront.IResponseHeadersPolicy</code> | Use this managed policy to allow simple CORS requests from any origin. |
| <code><a href="#cdk-constructs.ThronResponseHeaderPolicy.property.CORS_ALLOW_ALL_ORIGINS_AND_SECURITY_HEADERS">CORS_ALLOW_ALL_ORIGINS_AND_SECURITY_HEADERS</a></code> | <code>aws-cdk-lib.aws_cloudfront.IResponseHeadersPolicy</code> | Use this managed policy to allow simple CORS requests from any origin and add a set of security headers to all responses that CloudFront sends to viewers. |
| <code><a href="#cdk-constructs.ThronResponseHeaderPolicy.property.CORS_ALLOW_ALL_ORIGINS_WITH_PREFLIGHT">CORS_ALLOW_ALL_ORIGINS_WITH_PREFLIGHT</a></code> | <code>aws-cdk-lib.aws_cloudfront.IResponseHeadersPolicy</code> | Use this managed policy to allow CORS requests from any origin, including preflight requests. |
| <code><a href="#cdk-constructs.ThronResponseHeaderPolicy.property.CORS_ALLOW_ALL_ORIGINS_WITH_PREFLIGHT_AND_SECURITY_HEADERS">CORS_ALLOW_ALL_ORIGINS_WITH_PREFLIGHT_AND_SECURITY_HEADERS</a></code> | <code>aws-cdk-lib.aws_cloudfront.IResponseHeadersPolicy</code> | Use this managed policy to allow CORS requests from any origin, including preflight requests, and add a set of security headers to all responses that CloudFront sends to viewers. |
| <code><a href="#cdk-constructs.ThronResponseHeaderPolicy.property.SECURITY_HEADERS">SECURITY_HEADERS</a></code> | <code>aws-cdk-lib.aws_cloudfront.IResponseHeadersPolicy</code> | Use this managed policy to add a set of security headers to all responses that CloudFront sends to viewers. |

---

##### `CORS_ALLOW_ALL_ORIGINS`<sup>Required</sup> <a name="CORS_ALLOW_ALL_ORIGINS" id="cdk-constructs.ThronResponseHeaderPolicy.property.CORS_ALLOW_ALL_ORIGINS"></a>

```typescript
public readonly CORS_ALLOW_ALL_ORIGINS: IResponseHeadersPolicy;
```

- *Type:* aws-cdk-lib.aws_cloudfront.IResponseHeadersPolicy

Use this managed policy to allow simple CORS requests from any origin.

---

##### `CORS_ALLOW_ALL_ORIGINS_AND_SECURITY_HEADERS`<sup>Required</sup> <a name="CORS_ALLOW_ALL_ORIGINS_AND_SECURITY_HEADERS" id="cdk-constructs.ThronResponseHeaderPolicy.property.CORS_ALLOW_ALL_ORIGINS_AND_SECURITY_HEADERS"></a>

```typescript
public readonly CORS_ALLOW_ALL_ORIGINS_AND_SECURITY_HEADERS: IResponseHeadersPolicy;
```

- *Type:* aws-cdk-lib.aws_cloudfront.IResponseHeadersPolicy

Use this managed policy to allow simple CORS requests from any origin and add a set of security headers to all responses that CloudFront sends to viewers.

---

##### `CORS_ALLOW_ALL_ORIGINS_WITH_PREFLIGHT`<sup>Required</sup> <a name="CORS_ALLOW_ALL_ORIGINS_WITH_PREFLIGHT" id="cdk-constructs.ThronResponseHeaderPolicy.property.CORS_ALLOW_ALL_ORIGINS_WITH_PREFLIGHT"></a>

```typescript
public readonly CORS_ALLOW_ALL_ORIGINS_WITH_PREFLIGHT: IResponseHeadersPolicy;
```

- *Type:* aws-cdk-lib.aws_cloudfront.IResponseHeadersPolicy

Use this managed policy to allow CORS requests from any origin, including preflight requests.

---

##### `CORS_ALLOW_ALL_ORIGINS_WITH_PREFLIGHT_AND_SECURITY_HEADERS`<sup>Required</sup> <a name="CORS_ALLOW_ALL_ORIGINS_WITH_PREFLIGHT_AND_SECURITY_HEADERS" id="cdk-constructs.ThronResponseHeaderPolicy.property.CORS_ALLOW_ALL_ORIGINS_WITH_PREFLIGHT_AND_SECURITY_HEADERS"></a>

```typescript
public readonly CORS_ALLOW_ALL_ORIGINS_WITH_PREFLIGHT_AND_SECURITY_HEADERS: IResponseHeadersPolicy;
```

- *Type:* aws-cdk-lib.aws_cloudfront.IResponseHeadersPolicy

Use this managed policy to allow CORS requests from any origin, including preflight requests, and add a set of security headers to all responses that CloudFront sends to viewers.

---

##### `SECURITY_HEADERS`<sup>Required</sup> <a name="SECURITY_HEADERS" id="cdk-constructs.ThronResponseHeaderPolicy.property.SECURITY_HEADERS"></a>

```typescript
public readonly SECURITY_HEADERS: IResponseHeadersPolicy;
```

- *Type:* aws-cdk-lib.aws_cloudfront.IResponseHeadersPolicy

Use this managed policy to add a set of security headers to all responses that CloudFront sends to viewers.

---

### ThronStack <a name="ThronStack" id="cdk-constructs.ThronStack"></a>

#### Initializers <a name="Initializers" id="cdk-constructs.ThronStack.Initializer"></a>

```typescript
import { ThronStack } from 'cdk-constructs'

new ThronStack(scope: App, description?: string, suffix?: string, overrideAccount?: string, overrideRegion?: string)
```

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.ThronStack.Initializer.parameter.scope">scope</a></code> | <code>aws-cdk-lib.App</code> | *No description.* |
| <code><a href="#cdk-constructs.ThronStack.Initializer.parameter.description">description</a></code> | <code>string</code> | *No description.* |
| <code><a href="#cdk-constructs.ThronStack.Initializer.parameter.suffix">suffix</a></code> | <code>string</code> | *No description.* |
| <code><a href="#cdk-constructs.ThronStack.Initializer.parameter.overrideAccount">overrideAccount</a></code> | <code>string</code> | *No description.* |
| <code><a href="#cdk-constructs.ThronStack.Initializer.parameter.overrideRegion">overrideRegion</a></code> | <code>string</code> | *No description.* |

---

##### `scope`<sup>Required</sup> <a name="scope" id="cdk-constructs.ThronStack.Initializer.parameter.scope"></a>

- *Type:* aws-cdk-lib.App

---

##### `description`<sup>Optional</sup> <a name="description" id="cdk-constructs.ThronStack.Initializer.parameter.description"></a>

- *Type:* string

---

##### `suffix`<sup>Optional</sup> <a name="suffix" id="cdk-constructs.ThronStack.Initializer.parameter.suffix"></a>

- *Type:* string

---

##### `overrideAccount`<sup>Optional</sup> <a name="overrideAccount" id="cdk-constructs.ThronStack.Initializer.parameter.overrideAccount"></a>

- *Type:* string

---

##### `overrideRegion`<sup>Optional</sup> <a name="overrideRegion" id="cdk-constructs.ThronStack.Initializer.parameter.overrideRegion"></a>

- *Type:* string

---

#### Methods <a name="Methods" id="Methods"></a>

| **Name** | **Description** |
| --- | --- |
| <code><a href="#cdk-constructs.ThronStack.toString">toString</a></code> | Returns a string representation of this construct. |
| <code><a href="#cdk-constructs.ThronStack.addDependency">addDependency</a></code> | Add a dependency between this stack and another stack. |
| <code><a href="#cdk-constructs.ThronStack.addMetadata">addMetadata</a></code> | Adds an arbitrary key-value pair, with information you want to record about the stack. |
| <code><a href="#cdk-constructs.ThronStack.addTransform">addTransform</a></code> | Add a Transform to this stack. A Transform is a macro that AWS CloudFormation uses to process your template. |
| <code><a href="#cdk-constructs.ThronStack.exportStringListValue">exportStringListValue</a></code> | Create a CloudFormation Export for a string list value. |
| <code><a href="#cdk-constructs.ThronStack.exportValue">exportValue</a></code> | Create a CloudFormation Export for a string value. |
| <code><a href="#cdk-constructs.ThronStack.formatArn">formatArn</a></code> | Creates an ARN from components. |
| <code><a href="#cdk-constructs.ThronStack.getLogicalId">getLogicalId</a></code> | Allocates a stack-unique CloudFormation-compatible logical identity for a specific resource. |
| <code><a href="#cdk-constructs.ThronStack.regionalFact">regionalFact</a></code> | Look up a fact value for the given fact for the region of this stack. |
| <code><a href="#cdk-constructs.ThronStack.renameLogicalId">renameLogicalId</a></code> | Rename a generated logical identities. |
| <code><a href="#cdk-constructs.ThronStack.reportMissingContextKey">reportMissingContextKey</a></code> | Indicate that a context key was expected. |
| <code><a href="#cdk-constructs.ThronStack.resolve">resolve</a></code> | Resolve a tokenized value in the context of the current stack. |
| <code><a href="#cdk-constructs.ThronStack.splitArn">splitArn</a></code> | Splits the provided ARN into its components. |
| <code><a href="#cdk-constructs.ThronStack.toJsonString">toJsonString</a></code> | Convert an object, potentially containing tokens, to a JSON string. |
| <code><a href="#cdk-constructs.ThronStack.toYamlString">toYamlString</a></code> | Convert an object, potentially containing tokens, to a YAML string. |

---

##### `toString` <a name="toString" id="cdk-constructs.ThronStack.toString"></a>

```typescript
public toString(): string
```

Returns a string representation of this construct.

##### `addDependency` <a name="addDependency" id="cdk-constructs.ThronStack.addDependency"></a>

```typescript
public addDependency(target: Stack, reason?: string): void
```

Add a dependency between this stack and another stack.

This can be used to define dependencies between any two stacks within an
app, and also supports nested stacks.

###### `target`<sup>Required</sup> <a name="target" id="cdk-constructs.ThronStack.addDependency.parameter.target"></a>

- *Type:* aws-cdk-lib.Stack

---

###### `reason`<sup>Optional</sup> <a name="reason" id="cdk-constructs.ThronStack.addDependency.parameter.reason"></a>

- *Type:* string

---

##### `addMetadata` <a name="addMetadata" id="cdk-constructs.ThronStack.addMetadata"></a>

```typescript
public addMetadata(key: string, value: any): void
```

Adds an arbitrary key-value pair, with information you want to record about the stack.

These get translated to the Metadata section of the generated template.

> [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/metadata-section-structure.html](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/metadata-section-structure.html)

###### `key`<sup>Required</sup> <a name="key" id="cdk-constructs.ThronStack.addMetadata.parameter.key"></a>

- *Type:* string

---

###### `value`<sup>Required</sup> <a name="value" id="cdk-constructs.ThronStack.addMetadata.parameter.value"></a>

- *Type:* any

---

##### `addTransform` <a name="addTransform" id="cdk-constructs.ThronStack.addTransform"></a>

```typescript
public addTransform(transform: string): void
```

Add a Transform to this stack. A Transform is a macro that AWS CloudFormation uses to process your template.

Duplicate values are removed when stack is synthesized.

> [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/transform-section-structure.html](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/transform-section-structure.html)

*Example*

```typescript
declare const stack: Stack;

stack.addTransform('AWS::Serverless-2016-10-31')
```


###### `transform`<sup>Required</sup> <a name="transform" id="cdk-constructs.ThronStack.addTransform.parameter.transform"></a>

- *Type:* string

The transform to add.

---

##### `exportStringListValue` <a name="exportStringListValue" id="cdk-constructs.ThronStack.exportStringListValue"></a>

```typescript
public exportStringListValue(exportedValue: any, options?: ExportValueOptions): string[]
```

Create a CloudFormation Export for a string list value.

Returns a string list representing the corresponding `Fn.importValue()`
expression for this Export. The export expression is automatically wrapped with an
`Fn::Join` and the import value with an `Fn::Split`, since CloudFormation can only
export strings. You can control the name for the export by passing the `name` option.

If you don't supply a value for `name`, the value you're exporting must be
a Resource attribute (for example: `bucket.bucketName`) and it will be
given the same name as the automatic cross-stack reference that would be created
if you used the attribute in another Stack.

One of the uses for this method is to *remove* the relationship between
two Stacks established by automatic cross-stack references. It will
temporarily ensure that the CloudFormation Export still exists while you
remove the reference from the consuming stack. After that, you can remove
the resource and the manual export.

See `exportValue` for an example of this process.

###### `exportedValue`<sup>Required</sup> <a name="exportedValue" id="cdk-constructs.ThronStack.exportStringListValue.parameter.exportedValue"></a>

- *Type:* any

---

###### `options`<sup>Optional</sup> <a name="options" id="cdk-constructs.ThronStack.exportStringListValue.parameter.options"></a>

- *Type:* aws-cdk-lib.ExportValueOptions

---

##### `exportValue` <a name="exportValue" id="cdk-constructs.ThronStack.exportValue"></a>

```typescript
public exportValue(exportedValue: any, options?: ExportValueOptions): string
```

Create a CloudFormation Export for a string value.

Returns a string representing the corresponding `Fn.importValue()`
expression for this Export. You can control the name for the export by
passing the `name` option.

If you don't supply a value for `name`, the value you're exporting must be
a Resource attribute (for example: `bucket.bucketName`) and it will be
given the same name as the automatic cross-stack reference that would be created
if you used the attribute in another Stack.

One of the uses for this method is to *remove* the relationship between
two Stacks established by automatic cross-stack references. It will
temporarily ensure that the CloudFormation Export still exists while you
remove the reference from the consuming stack. After that, you can remove
the resource and the manual export.

Here is how the process works. Let's say there are two stacks,
`producerStack` and `consumerStack`, and `producerStack` has a bucket
called `bucket`, which is referenced by `consumerStack` (perhaps because
an AWS Lambda Function writes into it, or something like that).

It is not safe to remove `producerStack.bucket` because as the bucket is being
deleted, `consumerStack` might still be using it.

Instead, the process takes two deployments:

**Deployment 1: break the relationship**:

- Make sure `consumerStack` no longer references `bucket.bucketName` (maybe the consumer
  stack now uses its own bucket, or it writes to an AWS DynamoDB table, or maybe you just
  remove the Lambda Function altogether).
- In the `ProducerStack` class, call `this.exportValue(this.bucket.bucketName)`. This
  will make sure the CloudFormation Export continues to exist while the relationship
  between the two stacks is being broken.
- Deploy (this will effectively only change the `consumerStack`, but it's safe to deploy both).

**Deployment 2: remove the bucket resource**:

- You are now free to remove the `bucket` resource from `producerStack`.
- Don't forget to remove the `exportValue()` call as well.
- Deploy again (this time only the `producerStack` will be changed -- the bucket will be deleted).

###### `exportedValue`<sup>Required</sup> <a name="exportedValue" id="cdk-constructs.ThronStack.exportValue.parameter.exportedValue"></a>

- *Type:* any

---

###### `options`<sup>Optional</sup> <a name="options" id="cdk-constructs.ThronStack.exportValue.parameter.options"></a>

- *Type:* aws-cdk-lib.ExportValueOptions

---

##### `formatArn` <a name="formatArn" id="cdk-constructs.ThronStack.formatArn"></a>

```typescript
public formatArn(components: ArnComponents): string
```

Creates an ARN from components.

If `partition`, `region` or `account` are not specified, the stack's
partition, region and account will be used.

If any component is the empty string, an empty string will be inserted
into the generated ARN at the location that component corresponds to.

The ARN will be formatted as follows:

  arn:{partition}:{service}:{region}:{account}:{resource}{sep}{resource-name}

The required ARN pieces that are omitted will be taken from the stack that
the 'scope' is attached to. If all ARN pieces are supplied, the supplied scope
can be 'undefined'.

###### `components`<sup>Required</sup> <a name="components" id="cdk-constructs.ThronStack.formatArn.parameter.components"></a>

- *Type:* aws-cdk-lib.ArnComponents

---

##### `getLogicalId` <a name="getLogicalId" id="cdk-constructs.ThronStack.getLogicalId"></a>

```typescript
public getLogicalId(element: CfnElement): string
```

Allocates a stack-unique CloudFormation-compatible logical identity for a specific resource.

This method is called when a `CfnElement` is created and used to render the
initial logical identity of resources. Logical ID renames are applied at
this stage.

This method uses the protected method `allocateLogicalId` to render the
logical ID for an element. To modify the naming scheme, extend the `Stack`
class and override this method.

###### `element`<sup>Required</sup> <a name="element" id="cdk-constructs.ThronStack.getLogicalId.parameter.element"></a>

- *Type:* aws-cdk-lib.CfnElement

The CloudFormation element for which a logical identity is needed.

---

##### `regionalFact` <a name="regionalFact" id="cdk-constructs.ThronStack.regionalFact"></a>

```typescript
public regionalFact(factName: string, defaultValue?: string): string
```

Look up a fact value for the given fact for the region of this stack.

Will return a definite value only if the region of the current stack is resolved.
If not, a lookup map will be added to the stack and the lookup will be done at
CDK deployment time.

What regions will be included in the lookup map is controlled by the
`@aws-cdk/core:target-partitions` context value: it must be set to a list
of partitions, and only regions from the given partitions will be included.
If no such context key is set, all regions will be included.

This function is intended to be used by construct library authors. Application
builders can rely on the abstractions offered by construct libraries and do
not have to worry about regional facts.

If `defaultValue` is not given, it is an error if the fact is unknown for
the given region.

###### `factName`<sup>Required</sup> <a name="factName" id="cdk-constructs.ThronStack.regionalFact.parameter.factName"></a>

- *Type:* string

---

###### `defaultValue`<sup>Optional</sup> <a name="defaultValue" id="cdk-constructs.ThronStack.regionalFact.parameter.defaultValue"></a>

- *Type:* string

---

##### `renameLogicalId` <a name="renameLogicalId" id="cdk-constructs.ThronStack.renameLogicalId"></a>

```typescript
public renameLogicalId(oldId: string, newId: string): void
```

Rename a generated logical identities.

To modify the naming scheme strategy, extend the `Stack` class and
override the `allocateLogicalId` method.

###### `oldId`<sup>Required</sup> <a name="oldId" id="cdk-constructs.ThronStack.renameLogicalId.parameter.oldId"></a>

- *Type:* string

---

###### `newId`<sup>Required</sup> <a name="newId" id="cdk-constructs.ThronStack.renameLogicalId.parameter.newId"></a>

- *Type:* string

---

##### `reportMissingContextKey` <a name="reportMissingContextKey" id="cdk-constructs.ThronStack.reportMissingContextKey"></a>

```typescript
public reportMissingContextKey(report: MissingContext): void
```

Indicate that a context key was expected.

Contains instructions which will be emitted into the cloud assembly on how
the key should be supplied.

###### `report`<sup>Required</sup> <a name="report" id="cdk-constructs.ThronStack.reportMissingContextKey.parameter.report"></a>

- *Type:* aws-cdk-lib.cloud_assembly_schema.MissingContext

The set of parameters needed to obtain the context.

---

##### `resolve` <a name="resolve" id="cdk-constructs.ThronStack.resolve"></a>

```typescript
public resolve(obj: any): any
```

Resolve a tokenized value in the context of the current stack.

###### `obj`<sup>Required</sup> <a name="obj" id="cdk-constructs.ThronStack.resolve.parameter.obj"></a>

- *Type:* any

---

##### `splitArn` <a name="splitArn" id="cdk-constructs.ThronStack.splitArn"></a>

```typescript
public splitArn(arn: string, arnFormat: ArnFormat): ArnComponents
```

Splits the provided ARN into its components.

Works both if 'arn' is a string like 'arn:aws:s3:::bucket',
and a Token representing a dynamic CloudFormation expression
(in which case the returned components will also be dynamic CloudFormation expressions,
encoded as Tokens).

###### `arn`<sup>Required</sup> <a name="arn" id="cdk-constructs.ThronStack.splitArn.parameter.arn"></a>

- *Type:* string

the ARN to split into its components.

---

###### `arnFormat`<sup>Required</sup> <a name="arnFormat" id="cdk-constructs.ThronStack.splitArn.parameter.arnFormat"></a>

- *Type:* aws-cdk-lib.ArnFormat

the expected format of 'arn' - depends on what format the service 'arn' represents uses.

---

##### `toJsonString` <a name="toJsonString" id="cdk-constructs.ThronStack.toJsonString"></a>

```typescript
public toJsonString(obj: any, space?: number): string
```

Convert an object, potentially containing tokens, to a JSON string.

###### `obj`<sup>Required</sup> <a name="obj" id="cdk-constructs.ThronStack.toJsonString.parameter.obj"></a>

- *Type:* any

---

###### `space`<sup>Optional</sup> <a name="space" id="cdk-constructs.ThronStack.toJsonString.parameter.space"></a>

- *Type:* number

---

##### `toYamlString` <a name="toYamlString" id="cdk-constructs.ThronStack.toYamlString"></a>

```typescript
public toYamlString(obj: any): string
```

Convert an object, potentially containing tokens, to a YAML string.

###### `obj`<sup>Required</sup> <a name="obj" id="cdk-constructs.ThronStack.toYamlString.parameter.obj"></a>

- *Type:* any

---

#### Static Functions <a name="Static Functions" id="Static Functions"></a>

| **Name** | **Description** |
| --- | --- |
| <code><a href="#cdk-constructs.ThronStack.isConstruct">isConstruct</a></code> | Checks if `x` is a construct. |
| <code><a href="#cdk-constructs.ThronStack.isStack">isStack</a></code> | Return whether the given object is a Stack. |
| <code><a href="#cdk-constructs.ThronStack.of">of</a></code> | Looks up the first stack scope in which `construct` is defined. |

---

##### `isConstruct` <a name="isConstruct" id="cdk-constructs.ThronStack.isConstruct"></a>

```typescript
import { ThronStack } from 'cdk-constructs'

ThronStack.isConstruct(x: any)
```

Checks if `x` is a construct.

Use this method instead of `instanceof` to properly detect `Construct`
instances, even when the construct library is symlinked.

Explanation: in JavaScript, multiple copies of the `constructs` library on
disk are seen as independent, completely different libraries. As a
consequence, the class `Construct` in each copy of the `constructs` library
is seen as a different class, and an instance of one class will not test as
`instanceof` the other class. `npm install` will not create installations
like this, but users may manually symlink construct libraries together or
use a monorepo tool: in those cases, multiple copies of the `constructs`
library can be accidentally installed, and `instanceof` will behave
unpredictably. It is safest to avoid using `instanceof`, and using
this type-testing method instead.

###### `x`<sup>Required</sup> <a name="x" id="cdk-constructs.ThronStack.isConstruct.parameter.x"></a>

- *Type:* any

Any object.

---

##### `isStack` <a name="isStack" id="cdk-constructs.ThronStack.isStack"></a>

```typescript
import { ThronStack } from 'cdk-constructs'

ThronStack.isStack(x: any)
```

Return whether the given object is a Stack.

We do attribute detection since we can't reliably use 'instanceof'.

###### `x`<sup>Required</sup> <a name="x" id="cdk-constructs.ThronStack.isStack.parameter.x"></a>

- *Type:* any

---

##### `of` <a name="of" id="cdk-constructs.ThronStack.of"></a>

```typescript
import { ThronStack } from 'cdk-constructs'

ThronStack.of(construct: IConstruct)
```

Looks up the first stack scope in which `construct` is defined.

Fails if there is no stack up the tree.

###### `construct`<sup>Required</sup> <a name="construct" id="cdk-constructs.ThronStack.of.parameter.construct"></a>

- *Type:* constructs.IConstruct

The construct to start the search from.

---

#### Properties <a name="Properties" id="Properties"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.ThronStack.property.node">node</a></code> | <code>constructs.Node</code> | The tree node. |
| <code><a href="#cdk-constructs.ThronStack.property.account">account</a></code> | <code>string</code> | The AWS account into which this stack will be deployed. |
| <code><a href="#cdk-constructs.ThronStack.property.artifactId">artifactId</a></code> | <code>string</code> | The ID of the cloud assembly artifact for this stack. |
| <code><a href="#cdk-constructs.ThronStack.property.availabilityZones">availabilityZones</a></code> | <code>string[]</code> | Returns the list of AZs that are available in the AWS environment (account/region) associated with this stack. |
| <code><a href="#cdk-constructs.ThronStack.property.bundlingRequired">bundlingRequired</a></code> | <code>boolean</code> | Indicates whether the stack requires bundling or not. |
| <code><a href="#cdk-constructs.ThronStack.property.dependencies">dependencies</a></code> | <code>aws-cdk-lib.Stack[]</code> | Return the stacks this stack depends on. |
| <code><a href="#cdk-constructs.ThronStack.property.environment">environment</a></code> | <code>string</code> | The environment coordinates in which this stack is deployed. |
| <code><a href="#cdk-constructs.ThronStack.property.nested">nested</a></code> | <code>boolean</code> | Indicates if this is a nested stack, in which case `parentStack` will include a reference to it's parent. |
| <code><a href="#cdk-constructs.ThronStack.property.notificationArns">notificationArns</a></code> | <code>string[]</code> | Returns the list of notification Amazon Resource Names (ARNs) for the current stack. |
| <code><a href="#cdk-constructs.ThronStack.property.partition">partition</a></code> | <code>string</code> | The partition in which this stack is defined. |
| <code><a href="#cdk-constructs.ThronStack.property.region">region</a></code> | <code>string</code> | The AWS region into which this stack will be deployed (e.g. `us-west-2`). |
| <code><a href="#cdk-constructs.ThronStack.property.stackId">stackId</a></code> | <code>string</code> | The ID of the stack. |
| <code><a href="#cdk-constructs.ThronStack.property.stackName">stackName</a></code> | <code>string</code> | The concrete CloudFormation physical stack name. |
| <code><a href="#cdk-constructs.ThronStack.property.synthesizer">synthesizer</a></code> | <code>aws-cdk-lib.IStackSynthesizer</code> | Synthesis method for this stack. |
| <code><a href="#cdk-constructs.ThronStack.property.tags">tags</a></code> | <code>aws-cdk-lib.TagManager</code> | Tags to be applied to the stack. |
| <code><a href="#cdk-constructs.ThronStack.property.templateFile">templateFile</a></code> | <code>string</code> | The name of the CloudFormation template file emitted to the output directory during synthesis. |
| <code><a href="#cdk-constructs.ThronStack.property.templateOptions">templateOptions</a></code> | <code>aws-cdk-lib.ITemplateOptions</code> | Options for CloudFormation template (like version, transform, description). |
| <code><a href="#cdk-constructs.ThronStack.property.urlSuffix">urlSuffix</a></code> | <code>string</code> | The Amazon domain suffix for the region in which this stack is defined. |
| <code><a href="#cdk-constructs.ThronStack.property.nestedStackParent">nestedStackParent</a></code> | <code>aws-cdk-lib.Stack</code> | If this is a nested stack, returns it's parent stack. |
| <code><a href="#cdk-constructs.ThronStack.property.nestedStackResource">nestedStackResource</a></code> | <code>aws-cdk-lib.CfnResource</code> | If this is a nested stack, this represents its `AWS::CloudFormation::Stack` resource. |
| <code><a href="#cdk-constructs.ThronStack.property.terminationProtection">terminationProtection</a></code> | <code>boolean</code> | Whether termination protection is enabled for this stack. |
| <code><a href="#cdk-constructs.ThronStack.property.defaultValue">defaultValue</a></code> | <code><a href="#cdk-constructs.DefaultValue">DefaultValue</a></code> | *No description.* |
| <code><a href="#cdk-constructs.ThronStack.property.projectId">projectId</a></code> | <code>string</code> | *No description.* |
| <code><a href="#cdk-constructs.ThronStack.property.thronEnvironment">thronEnvironment</a></code> | <code>string</code> | *No description.* |
| <code><a href="#cdk-constructs.ThronStack.property.thronSitename">thronSitename</a></code> | <code>string</code> | *No description.* |

---

##### `node`<sup>Required</sup> <a name="node" id="cdk-constructs.ThronStack.property.node"></a>

```typescript
public readonly node: Node;
```

- *Type:* constructs.Node

The tree node.

---

##### `account`<sup>Required</sup> <a name="account" id="cdk-constructs.ThronStack.property.account"></a>

```typescript
public readonly account: string;
```

- *Type:* string

The AWS account into which this stack will be deployed.

This value is resolved according to the following rules:

1. The value provided to `env.account` when the stack is defined. This can
   either be a concrete account (e.g. `585695031111`) or the
   `Aws.ACCOUNT_ID` token.
3. `Aws.ACCOUNT_ID`, which represents the CloudFormation intrinsic reference
   `{ "Ref": "AWS::AccountId" }` encoded as a string token.

Preferably, you should use the return value as an opaque string and not
attempt to parse it to implement your logic. If you do, you must first
check that it is a concrete value an not an unresolved token. If this
value is an unresolved token (`Token.isUnresolved(stack.account)` returns
`true`), this implies that the user wishes that this stack will synthesize
into an **account-agnostic template**. In this case, your code should either
fail (throw an error, emit a synth error using `Annotations.of(construct).addError()`) or
implement some other account-agnostic behavior.

---

##### `artifactId`<sup>Required</sup> <a name="artifactId" id="cdk-constructs.ThronStack.property.artifactId"></a>

```typescript
public readonly artifactId: string;
```

- *Type:* string

The ID of the cloud assembly artifact for this stack.

---

##### `availabilityZones`<sup>Required</sup> <a name="availabilityZones" id="cdk-constructs.ThronStack.property.availabilityZones"></a>

```typescript
public readonly availabilityZones: string[];
```

- *Type:* string[]

Returns the list of AZs that are available in the AWS environment (account/region) associated with this stack.

If the stack is environment-agnostic (either account and/or region are
tokens), this property will return an array with 2 tokens that will resolve
at deploy-time to the first two availability zones returned from CloudFormation's
`Fn::GetAZs` intrinsic function.

If they are not available in the context, returns a set of dummy values and
reports them as missing, and let the CLI resolve them by calling EC2
`DescribeAvailabilityZones` on the target environment.

To specify a different strategy for selecting availability zones override this method.

---

##### `bundlingRequired`<sup>Required</sup> <a name="bundlingRequired" id="cdk-constructs.ThronStack.property.bundlingRequired"></a>

```typescript
public readonly bundlingRequired: boolean;
```

- *Type:* boolean

Indicates whether the stack requires bundling or not.

---

##### `dependencies`<sup>Required</sup> <a name="dependencies" id="cdk-constructs.ThronStack.property.dependencies"></a>

```typescript
public readonly dependencies: Stack[];
```

- *Type:* aws-cdk-lib.Stack[]

Return the stacks this stack depends on.

---

##### `environment`<sup>Required</sup> <a name="environment" id="cdk-constructs.ThronStack.property.environment"></a>

```typescript
public readonly environment: string;
```

- *Type:* string

The environment coordinates in which this stack is deployed.

In the form
`aws://account/region`. Use `stack.account` and `stack.region` to obtain
the specific values, no need to parse.

You can use this value to determine if two stacks are targeting the same
environment.

If either `stack.account` or `stack.region` are not concrete values (e.g.
`Aws.ACCOUNT_ID` or `Aws.REGION`) the special strings `unknown-account` and/or
`unknown-region` will be used respectively to indicate this stack is
region/account-agnostic.

---

##### `nested`<sup>Required</sup> <a name="nested" id="cdk-constructs.ThronStack.property.nested"></a>

```typescript
public readonly nested: boolean;
```

- *Type:* boolean

Indicates if this is a nested stack, in which case `parentStack` will include a reference to it's parent.

---

##### `notificationArns`<sup>Required</sup> <a name="notificationArns" id="cdk-constructs.ThronStack.property.notificationArns"></a>

```typescript
public readonly notificationArns: string[];
```

- *Type:* string[]

Returns the list of notification Amazon Resource Names (ARNs) for the current stack.

---

##### `partition`<sup>Required</sup> <a name="partition" id="cdk-constructs.ThronStack.property.partition"></a>

```typescript
public readonly partition: string;
```

- *Type:* string

The partition in which this stack is defined.

---

##### `region`<sup>Required</sup> <a name="region" id="cdk-constructs.ThronStack.property.region"></a>

```typescript
public readonly region: string;
```

- *Type:* string

The AWS region into which this stack will be deployed (e.g. `us-west-2`).

This value is resolved according to the following rules:

1. The value provided to `env.region` when the stack is defined. This can
   either be a concrete region (e.g. `us-west-2`) or the `Aws.REGION`
   token.
3. `Aws.REGION`, which is represents the CloudFormation intrinsic reference
   `{ "Ref": "AWS::Region" }` encoded as a string token.

Preferably, you should use the return value as an opaque string and not
attempt to parse it to implement your logic. If you do, you must first
check that it is a concrete value an not an unresolved token. If this
value is an unresolved token (`Token.isUnresolved(stack.region)` returns
`true`), this implies that the user wishes that this stack will synthesize
into a **region-agnostic template**. In this case, your code should either
fail (throw an error, emit a synth error using `Annotations.of(construct).addError()`) or
implement some other region-agnostic behavior.

---

##### `stackId`<sup>Required</sup> <a name="stackId" id="cdk-constructs.ThronStack.property.stackId"></a>

```typescript
public readonly stackId: string;
```

- *Type:* string

The ID of the stack.

---

*Example*

```typescript
// After resolving, looks like
'arn:aws:cloudformation:us-west-2:123456789012:stack/teststack/51af3dc0-da77-11e4-872e-1234567db123'
```


##### `stackName`<sup>Required</sup> <a name="stackName" id="cdk-constructs.ThronStack.property.stackName"></a>

```typescript
public readonly stackName: string;
```

- *Type:* string

The concrete CloudFormation physical stack name.

This is either the name defined explicitly in the `stackName` prop or
allocated based on the stack's location in the construct tree. Stacks that
are directly defined under the app use their construct `id` as their stack
name. Stacks that are defined deeper within the tree will use a hashed naming
scheme based on the construct path to ensure uniqueness.

If you wish to obtain the deploy-time AWS::StackName intrinsic,
you can use `Aws.STACK_NAME` directly.

---

##### `synthesizer`<sup>Required</sup> <a name="synthesizer" id="cdk-constructs.ThronStack.property.synthesizer"></a>

```typescript
public readonly synthesizer: IStackSynthesizer;
```

- *Type:* aws-cdk-lib.IStackSynthesizer

Synthesis method for this stack.

---

##### `tags`<sup>Required</sup> <a name="tags" id="cdk-constructs.ThronStack.property.tags"></a>

```typescript
public readonly tags: TagManager;
```

- *Type:* aws-cdk-lib.TagManager

Tags to be applied to the stack.

---

##### `templateFile`<sup>Required</sup> <a name="templateFile" id="cdk-constructs.ThronStack.property.templateFile"></a>

```typescript
public readonly templateFile: string;
```

- *Type:* string

The name of the CloudFormation template file emitted to the output directory during synthesis.

Example value: `MyStack.template.json`

---

##### `templateOptions`<sup>Required</sup> <a name="templateOptions" id="cdk-constructs.ThronStack.property.templateOptions"></a>

```typescript
public readonly templateOptions: ITemplateOptions;
```

- *Type:* aws-cdk-lib.ITemplateOptions

Options for CloudFormation template (like version, transform, description).

---

##### `urlSuffix`<sup>Required</sup> <a name="urlSuffix" id="cdk-constructs.ThronStack.property.urlSuffix"></a>

```typescript
public readonly urlSuffix: string;
```

- *Type:* string

The Amazon domain suffix for the region in which this stack is defined.

---

##### `nestedStackParent`<sup>Optional</sup> <a name="nestedStackParent" id="cdk-constructs.ThronStack.property.nestedStackParent"></a>

```typescript
public readonly nestedStackParent: Stack;
```

- *Type:* aws-cdk-lib.Stack

If this is a nested stack, returns it's parent stack.

---

##### `nestedStackResource`<sup>Optional</sup> <a name="nestedStackResource" id="cdk-constructs.ThronStack.property.nestedStackResource"></a>

```typescript
public readonly nestedStackResource: CfnResource;
```

- *Type:* aws-cdk-lib.CfnResource

If this is a nested stack, this represents its `AWS::CloudFormation::Stack` resource.

`undefined` for top-level (non-nested) stacks.

---

##### `terminationProtection`<sup>Required</sup> <a name="terminationProtection" id="cdk-constructs.ThronStack.property.terminationProtection"></a>

```typescript
public readonly terminationProtection: boolean;
```

- *Type:* boolean

Whether termination protection is enabled for this stack.

---

##### `defaultValue`<sup>Required</sup> <a name="defaultValue" id="cdk-constructs.ThronStack.property.defaultValue"></a>

```typescript
public readonly defaultValue: DefaultValue;
```

- *Type:* <a href="#cdk-constructs.DefaultValue">DefaultValue</a>

---

##### `projectId`<sup>Required</sup> <a name="projectId" id="cdk-constructs.ThronStack.property.projectId"></a>

```typescript
public readonly projectId: string;
```

- *Type:* string

---

##### `thronEnvironment`<sup>Required</sup> <a name="thronEnvironment" id="cdk-constructs.ThronStack.property.thronEnvironment"></a>

```typescript
public readonly thronEnvironment: string;
```

- *Type:* string

---

##### `thronSitename`<sup>Required</sup> <a name="thronSitename" id="cdk-constructs.ThronStack.property.thronSitename"></a>

```typescript
public readonly thronSitename: string;
```

- *Type:* string

---


### ThronTargetScaling <a name="ThronTargetScaling" id="cdk-constructs.ThronTargetScaling"></a>

#### Initializers <a name="Initializers" id="cdk-constructs.ThronTargetScaling.Initializer"></a>

```typescript
import { ThronTargetScaling } from 'cdk-constructs'

new ThronTargetScaling(scope: Construct, id: string, props: ThronTargetScalingProps)
```

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.ThronTargetScaling.Initializer.parameter.scope">scope</a></code> | <code>constructs.Construct</code> | *No description.* |
| <code><a href="#cdk-constructs.ThronTargetScaling.Initializer.parameter.id">id</a></code> | <code>string</code> | *No description.* |
| <code><a href="#cdk-constructs.ThronTargetScaling.Initializer.parameter.props">props</a></code> | <code><a href="#cdk-constructs.ThronTargetScalingProps">ThronTargetScalingProps</a></code> | *No description.* |

---

##### `scope`<sup>Required</sup> <a name="scope" id="cdk-constructs.ThronTargetScaling.Initializer.parameter.scope"></a>

- *Type:* constructs.Construct

---

##### `id`<sup>Required</sup> <a name="id" id="cdk-constructs.ThronTargetScaling.Initializer.parameter.id"></a>

- *Type:* string

---

##### `props`<sup>Required</sup> <a name="props" id="cdk-constructs.ThronTargetScaling.Initializer.parameter.props"></a>

- *Type:* <a href="#cdk-constructs.ThronTargetScalingProps">ThronTargetScalingProps</a>

---

#### Methods <a name="Methods" id="Methods"></a>

| **Name** | **Description** |
| --- | --- |
| <code><a href="#cdk-constructs.ThronTargetScaling.toString">toString</a></code> | Returns a string representation of this construct. |

---

##### `toString` <a name="toString" id="cdk-constructs.ThronTargetScaling.toString"></a>

```typescript
public toString(): string
```

Returns a string representation of this construct.

#### Static Functions <a name="Static Functions" id="Static Functions"></a>

| **Name** | **Description** |
| --- | --- |
| <code><a href="#cdk-constructs.ThronTargetScaling.isConstruct">isConstruct</a></code> | Checks if `x` is a construct. |

---

##### `isConstruct` <a name="isConstruct" id="cdk-constructs.ThronTargetScaling.isConstruct"></a>

```typescript
import { ThronTargetScaling } from 'cdk-constructs'

ThronTargetScaling.isConstruct(x: any)
```

Checks if `x` is a construct.

Use this method instead of `instanceof` to properly detect `Construct`
instances, even when the construct library is symlinked.

Explanation: in JavaScript, multiple copies of the `constructs` library on
disk are seen as independent, completely different libraries. As a
consequence, the class `Construct` in each copy of the `constructs` library
is seen as a different class, and an instance of one class will not test as
`instanceof` the other class. `npm install` will not create installations
like this, but users may manually symlink construct libraries together or
use a monorepo tool: in those cases, multiple copies of the `constructs`
library can be accidentally installed, and `instanceof` will behave
unpredictably. It is safest to avoid using `instanceof`, and using
this type-testing method instead.

###### `x`<sup>Required</sup> <a name="x" id="cdk-constructs.ThronTargetScaling.isConstruct.parameter.x"></a>

- *Type:* any

Any object.

---

#### Properties <a name="Properties" id="Properties"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.ThronTargetScaling.property.node">node</a></code> | <code>constructs.Node</code> | The tree node. |
| <code><a href="#cdk-constructs.ThronTargetScaling.property.maxCapacity">maxCapacity</a></code> | <code>number</code> | The maximum value that Application Auto Scaling can use to scale a target during a scaling activity. |
| <code><a href="#cdk-constructs.ThronTargetScaling.property.minCapacity">minCapacity</a></code> | <code>number</code> | The minimum value that Application Auto Scaling can use to scale a target during a scaling activity. |
| <code><a href="#cdk-constructs.ThronTargetScaling.property.targetValue">targetValue</a></code> | <code>number</code> | The target value for the metric. |
| <code><a href="#cdk-constructs.ThronTargetScaling.property.predefinedMetric">predefinedMetric</a></code> | <code>aws-cdk-lib.aws_applicationautoscaling.PredefinedMetric</code> | A predefined metric for application autoscaling. |

---

##### `node`<sup>Required</sup> <a name="node" id="cdk-constructs.ThronTargetScaling.property.node"></a>

```typescript
public readonly node: Node;
```

- *Type:* constructs.Node

The tree node.

---

##### `maxCapacity`<sup>Required</sup> <a name="maxCapacity" id="cdk-constructs.ThronTargetScaling.property.maxCapacity"></a>

```typescript
public readonly maxCapacity: number;
```

- *Type:* number

The maximum value that Application Auto Scaling can use to scale a target during a scaling activity.

---

##### `minCapacity`<sup>Required</sup> <a name="minCapacity" id="cdk-constructs.ThronTargetScaling.property.minCapacity"></a>

```typescript
public readonly minCapacity: number;
```

- *Type:* number

The minimum value that Application Auto Scaling can use to scale a target during a scaling activity.

---

##### `targetValue`<sup>Required</sup> <a name="targetValue" id="cdk-constructs.ThronTargetScaling.property.targetValue"></a>

```typescript
public readonly targetValue: number;
```

- *Type:* number

The target value for the metric.

---

##### `predefinedMetric`<sup>Optional</sup> <a name="predefinedMetric" id="cdk-constructs.ThronTargetScaling.property.predefinedMetric"></a>

```typescript
public readonly predefinedMetric: PredefinedMetric;
```

- *Type:* aws-cdk-lib.aws_applicationautoscaling.PredefinedMetric

A predefined metric for application autoscaling.

The metric must track utilization. Scaling out will happen if the metric is higher than the target value,
scaling in will happen in the metric is lower than the target value.

---


### ThronVpc <a name="ThronVpc" id="cdk-constructs.ThronVpc"></a>

Construct for creating a DualsStack VPC with support for: - Dualstack - Vpc Endpoints - Vpc Peering - ... and many more.

More on the architecture here:
https://thron.atlassian.net/wiki/spaces/PPI/pages/1132888071/New+Network+Infrastructure+Proposal

*Example*

```typescript
   const vpc = new ThronVpc(this,'prova',{
   ipv4Cidr: '10.8.0.0/16',
   isNatHA: false,
   prefix: 'prova',
   gatewayEndpoints: [
     GatewayVpcEndpointAwsService.S3
   ],
   interfaceEndpoints: [InterfaceVpcEndpointAwsService.EC2],
   subnetsConfigs: [
     {
       availabilityZone: AvailabilityZone.A,
       ipv4Cidr: '10.8.192.0/20',
       ipv6CidrSlotNumber: 7,
       type: SubnetType.PUBLIC
     },
     {
       availabilityZone: AvailabilityZone.B,
       ipv4Cidr: '10.8.208.0/20',
       ipv6CidrSlotNumber: 8,
       type: SubnetType.PUBLIC
     },
     {
       availabilityZone: AvailabilityZone.C,
       ipv4Cidr: '10.8.224.0/20',
       ipv6CidrSlotNumber: 9,
       type: SubnetType.PUBLIC
     },
     //
     {
       availabilityZone: AvailabilityZone.A,
       ipv4Cidr: '10.8.0.0/18',
       ipv6CidrSlotNumber: 1,
       type: SubnetType.PRIVATE
     },
     {
       availabilityZone: AvailabilityZone.B,
       ipv4Cidr: '10.8.64.0/18',
       ipv6CidrSlotNumber: 2,
       type: SubnetType.PRIVATE
     },
     {
       availabilityZone: AvailabilityZone.C,
       ipv4Cidr: '10.8.128.0/18',
       ipv6CidrSlotNumber: 3,
       type: SubnetType.PRIVATE
     }
   ]
  })
```


#### Initializers <a name="Initializers" id="cdk-constructs.ThronVpc.Initializer"></a>

```typescript
import { ThronVpc } from 'cdk-constructs'

new ThronVpc(scope: Construct, id: string, props: ThronVpcProps)
```

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.ThronVpc.Initializer.parameter.scope">scope</a></code> | <code>constructs.Construct</code> | Construct on which to instantiate the VPC on. |
| <code><a href="#cdk-constructs.ThronVpc.Initializer.parameter.id">id</a></code> | <code>string</code> | Logical id of the construct. |
| <code><a href="#cdk-constructs.ThronVpc.Initializer.parameter.props">props</a></code> | <code><a href="#cdk-constructs.ThronVpcProps">ThronVpcProps</a></code> | *No description.* |

---

##### `scope`<sup>Required</sup> <a name="scope" id="cdk-constructs.ThronVpc.Initializer.parameter.scope"></a>

- *Type:* constructs.Construct

Construct on which to instantiate the VPC on.

---

##### `id`<sup>Required</sup> <a name="id" id="cdk-constructs.ThronVpc.Initializer.parameter.id"></a>

- *Type:* string

Logical id of the construct.

---

##### `props`<sup>Required</sup> <a name="props" id="cdk-constructs.ThronVpc.Initializer.parameter.props"></a>

- *Type:* <a href="#cdk-constructs.ThronVpcProps">ThronVpcProps</a>

---

#### Methods <a name="Methods" id="Methods"></a>

| **Name** | **Description** |
| --- | --- |
| <code><a href="#cdk-constructs.ThronVpc.toString">toString</a></code> | Returns a string representation of this construct. |
| <code><a href="#cdk-constructs.ThronVpc.addAtlasClusterPeering">addAtlasClusterPeering</a></code> | *No description.* |
| <code><a href="#cdk-constructs.ThronVpc.addPeeringFromOtherAccount">addPeeringFromOtherAccount</a></code> | Adds a peering with another VPC in another account, along with the routes. |
| <code><a href="#cdk-constructs.ThronVpc.addVpcPeering">addVpcPeering</a></code> | Adds a peering with another VPC, along with the routes. |

---

##### `toString` <a name="toString" id="cdk-constructs.ThronVpc.toString"></a>

```typescript
public toString(): string
```

Returns a string representation of this construct.

##### `addAtlasClusterPeering` <a name="addAtlasClusterPeering" id="cdk-constructs.ThronVpc.addAtlasClusterPeering"></a>

```typescript
public addAtlasClusterPeering(peeringConf: AtlasPeeringConf): string
```

###### `peeringConf`<sup>Required</sup> <a name="peeringConf" id="cdk-constructs.ThronVpc.addAtlasClusterPeering.parameter.peeringConf"></a>

- *Type:* <a href="#cdk-constructs.AtlasPeeringConf">AtlasPeeringConf</a>

Configuration for the atlas peering.

---

##### `addPeeringFromOtherAccount` <a name="addPeeringFromOtherAccount" id="cdk-constructs.ThronVpc.addPeeringFromOtherAccount"></a>

```typescript
public addPeeringFromOtherAccount(peerConfig: OtherAccountPeeringConfig): string
```

Adds a peering with another VPC in another account, along with the routes.

###### `peerConfig`<sup>Required</sup> <a name="peerConfig" id="cdk-constructs.ThronVpc.addPeeringFromOtherAccount.parameter.peerConfig"></a>

- *Type:* <a href="#cdk-constructs.OtherAccountPeeringConfig">OtherAccountPeeringConfig</a>

Peering configuration.

---

##### `addVpcPeering` <a name="addVpcPeering" id="cdk-constructs.ThronVpc.addVpcPeering"></a>

```typescript
public addVpcPeering(peerConfig: PeeringConfig): void
```

Adds a peering with another VPC, along with the routes.

###### `peerConfig`<sup>Required</sup> <a name="peerConfig" id="cdk-constructs.ThronVpc.addVpcPeering.parameter.peerConfig"></a>

- *Type:* <a href="#cdk-constructs.PeeringConfig">PeeringConfig</a>

Peering configuration.

---

#### Static Functions <a name="Static Functions" id="Static Functions"></a>

| **Name** | **Description** |
| --- | --- |
| <code><a href="#cdk-constructs.ThronVpc.isConstruct">isConstruct</a></code> | Checks if `x` is a construct. |

---

##### `isConstruct` <a name="isConstruct" id="cdk-constructs.ThronVpc.isConstruct"></a>

```typescript
import { ThronVpc } from 'cdk-constructs'

ThronVpc.isConstruct(x: any)
```

Checks if `x` is a construct.

Use this method instead of `instanceof` to properly detect `Construct`
instances, even when the construct library is symlinked.

Explanation: in JavaScript, multiple copies of the `constructs` library on
disk are seen as independent, completely different libraries. As a
consequence, the class `Construct` in each copy of the `constructs` library
is seen as a different class, and an instance of one class will not test as
`instanceof` the other class. `npm install` will not create installations
like this, but users may manually symlink construct libraries together or
use a monorepo tool: in those cases, multiple copies of the `constructs`
library can be accidentally installed, and `instanceof` will behave
unpredictably. It is safest to avoid using `instanceof`, and using
this type-testing method instead.

###### `x`<sup>Required</sup> <a name="x" id="cdk-constructs.ThronVpc.isConstruct.parameter.x"></a>

- *Type:* any

Any object.

---

#### Properties <a name="Properties" id="Properties"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.ThronVpc.property.node">node</a></code> | <code>constructs.Node</code> | The tree node. |
| <code><a href="#cdk-constructs.ThronVpc.property.egressOnlyInternetGateway">egressOnlyInternetGateway</a></code> | <code>aws-cdk-lib.aws_ec2.CfnEgressOnlyInternetGateway</code> | *No description.* |
| <code><a href="#cdk-constructs.ThronVpc.property.gatewayEndpoints">gatewayEndpoints</a></code> | <code>aws-cdk-lib.aws_ec2.GatewayVpcEndpoint[]</code> | *No description.* |
| <code><a href="#cdk-constructs.ThronVpc.property.interfaceEndpoints">interfaceEndpoints</a></code> | <code>aws-cdk-lib.aws_ec2.InterfaceVpcEndpoint[]</code> | *No description.* |
| <code><a href="#cdk-constructs.ThronVpc.property.internetGateway">internetGateway</a></code> | <code>aws-cdk-lib.aws_ec2.CfnInternetGateway</code> | *No description.* |
| <code><a href="#cdk-constructs.ThronVpc.property.ipv4CidrBlock">ipv4CidrBlock</a></code> | <code>string</code> | *No description.* |
| <code><a href="#cdk-constructs.ThronVpc.property.ipv6CidrBlock">ipv6CidrBlock</a></code> | <code>string</code> | *No description.* |
| <code><a href="#cdk-constructs.ThronVpc.property.nats">nats</a></code> | <code>aws-cdk-lib.aws_ec2.CfnNatGateway[]</code> | *No description.* |
| <code><a href="#cdk-constructs.ThronVpc.property.prefix">prefix</a></code> | <code>string</code> | *No description.* |
| <code><a href="#cdk-constructs.ThronVpc.property.privateSubnets">privateSubnets</a></code> | <code>aws-cdk-lib.aws_ec2.Subnet[]</code> | *No description.* |
| <code><a href="#cdk-constructs.ThronVpc.property.publicSubnets">publicSubnets</a></code> | <code>aws-cdk-lib.aws_ec2.Subnet[]</code> | *No description.* |
| <code><a href="#cdk-constructs.ThronVpc.property.vpc">vpc</a></code> | <code>aws-cdk-lib.aws_ec2.Vpc</code> | *No description.* |

---

##### `node`<sup>Required</sup> <a name="node" id="cdk-constructs.ThronVpc.property.node"></a>

```typescript
public readonly node: Node;
```

- *Type:* constructs.Node

The tree node.

---

##### `egressOnlyInternetGateway`<sup>Required</sup> <a name="egressOnlyInternetGateway" id="cdk-constructs.ThronVpc.property.egressOnlyInternetGateway"></a>

```typescript
public readonly egressOnlyInternetGateway: CfnEgressOnlyInternetGateway;
```

- *Type:* aws-cdk-lib.aws_ec2.CfnEgressOnlyInternetGateway

---

##### `gatewayEndpoints`<sup>Required</sup> <a name="gatewayEndpoints" id="cdk-constructs.ThronVpc.property.gatewayEndpoints"></a>

```typescript
public readonly gatewayEndpoints: GatewayVpcEndpoint[];
```

- *Type:* aws-cdk-lib.aws_ec2.GatewayVpcEndpoint[]

---

##### `interfaceEndpoints`<sup>Required</sup> <a name="interfaceEndpoints" id="cdk-constructs.ThronVpc.property.interfaceEndpoints"></a>

```typescript
public readonly interfaceEndpoints: InterfaceVpcEndpoint[];
```

- *Type:* aws-cdk-lib.aws_ec2.InterfaceVpcEndpoint[]

---

##### `internetGateway`<sup>Required</sup> <a name="internetGateway" id="cdk-constructs.ThronVpc.property.internetGateway"></a>

```typescript
public readonly internetGateway: CfnInternetGateway;
```

- *Type:* aws-cdk-lib.aws_ec2.CfnInternetGateway

---

##### `ipv4CidrBlock`<sup>Required</sup> <a name="ipv4CidrBlock" id="cdk-constructs.ThronVpc.property.ipv4CidrBlock"></a>

```typescript
public readonly ipv4CidrBlock: string;
```

- *Type:* string

---

##### `ipv6CidrBlock`<sup>Required</sup> <a name="ipv6CidrBlock" id="cdk-constructs.ThronVpc.property.ipv6CidrBlock"></a>

```typescript
public readonly ipv6CidrBlock: string;
```

- *Type:* string

---

##### `nats`<sup>Required</sup> <a name="nats" id="cdk-constructs.ThronVpc.property.nats"></a>

```typescript
public readonly nats: CfnNatGateway[];
```

- *Type:* aws-cdk-lib.aws_ec2.CfnNatGateway[]

---

##### `prefix`<sup>Required</sup> <a name="prefix" id="cdk-constructs.ThronVpc.property.prefix"></a>

```typescript
public readonly prefix: string;
```

- *Type:* string

---

##### `privateSubnets`<sup>Required</sup> <a name="privateSubnets" id="cdk-constructs.ThronVpc.property.privateSubnets"></a>

```typescript
public readonly privateSubnets: Subnet[];
```

- *Type:* aws-cdk-lib.aws_ec2.Subnet[]

---

##### `publicSubnets`<sup>Required</sup> <a name="publicSubnets" id="cdk-constructs.ThronVpc.property.publicSubnets"></a>

```typescript
public readonly publicSubnets: Subnet[];
```

- *Type:* aws-cdk-lib.aws_ec2.Subnet[]

---

##### `vpc`<sup>Required</sup> <a name="vpc" id="cdk-constructs.ThronVpc.property.vpc"></a>

```typescript
public readonly vpc: Vpc;
```

- *Type:* aws-cdk-lib.aws_ec2.Vpc

---


## Structs <a name="Structs" id="Structs"></a>

### AtlasPeeringConf <a name="AtlasPeeringConf" id="cdk-constructs.AtlasPeeringConf"></a>

#### Initializer <a name="Initializer" id="cdk-constructs.AtlasPeeringConf.Initializer"></a>

```typescript
import { AtlasPeeringConf } from 'cdk-constructs'

const atlasPeeringConf: AtlasPeeringConf = { ... }
```

#### Properties <a name="Properties" id="Properties"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.AtlasPeeringConf.property.atlasCidr">atlasCidr</a></code> | <code>string</code> | Cidr notation of the atlas cluster. |
| <code><a href="#cdk-constructs.AtlasPeeringConf.property.atlasContainerId">atlasContainerId</a></code> | <code>string</code> | Id of the atlas network container. |
| <code><a href="#cdk-constructs.AtlasPeeringConf.property.atlasProjectId">atlasProjectId</a></code> | <code>string</code> | Id of the atlas project. |
| <code><a href="#cdk-constructs.AtlasPeeringConf.property.clusterName">clusterName</a></code> | <code>string</code> | Name of the cluster to be used as logical di. |

---

##### `atlasCidr`<sup>Required</sup> <a name="atlasCidr" id="cdk-constructs.AtlasPeeringConf.property.atlasCidr"></a>

```typescript
public readonly atlasCidr: string;
```

- *Type:* string

Cidr notation of the atlas cluster.

---

##### `atlasContainerId`<sup>Required</sup> <a name="atlasContainerId" id="cdk-constructs.AtlasPeeringConf.property.atlasContainerId"></a>

```typescript
public readonly atlasContainerId: string;
```

- *Type:* string

Id of the atlas network container.

---

##### `atlasProjectId`<sup>Required</sup> <a name="atlasProjectId" id="cdk-constructs.AtlasPeeringConf.property.atlasProjectId"></a>

```typescript
public readonly atlasProjectId: string;
```

- *Type:* string

Id of the atlas project.

---

##### `clusterName`<sup>Required</sup> <a name="clusterName" id="cdk-constructs.AtlasPeeringConf.property.clusterName"></a>

```typescript
public readonly clusterName: string;
```

- *Type:* string

Name of the cluster to be used as logical di.

---

### CicdEnvironment <a name="CicdEnvironment" id="cdk-constructs.CicdEnvironment"></a>

#### Initializer <a name="Initializer" id="cdk-constructs.CicdEnvironment.Initializer"></a>

```typescript
import { CicdEnvironment } from 'cdk-constructs'

const cicdEnvironment: CicdEnvironment = { ... }
```

#### Properties <a name="Properties" id="Properties"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.CicdEnvironment.property.capabilities">capabilities</a></code> | <code><a href="#cdk-constructs.PipelineCapability">PipelineCapability</a>[]</code> | *No description.* |
| <code><a href="#cdk-constructs.CicdEnvironment.property.webhookUrl">webhookUrl</a></code> | <code>string</code> | *No description.* |

---

##### `capabilities`<sup>Required</sup> <a name="capabilities" id="cdk-constructs.CicdEnvironment.property.capabilities"></a>

```typescript
public readonly capabilities: PipelineCapability[];
```

- *Type:* <a href="#cdk-constructs.PipelineCapability">PipelineCapability</a>[]

---

##### `webhookUrl`<sup>Optional</sup> <a name="webhookUrl" id="cdk-constructs.CicdEnvironment.property.webhookUrl"></a>

```typescript
public readonly webhookUrl: string;
```

- *Type:* string

---

### DeployConfig <a name="DeployConfig" id="cdk-constructs.DeployConfig"></a>

#### Initializer <a name="Initializer" id="cdk-constructs.DeployConfig.Initializer"></a>

```typescript
import { DeployConfig } from 'cdk-constructs'

const deployConfig: DeployConfig = { ... }
```

#### Properties <a name="Properties" id="Properties"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.DeployConfig.property.deploymentAwsAccount">deploymentAwsAccount</a></code> | <code>string</code> | *No description.* |
| <code><a href="#cdk-constructs.DeployConfig.property.deploymentAwsRegion">deploymentAwsRegion</a></code> | <code>string</code> | *No description.* |
| <code><a href="#cdk-constructs.DeployConfig.property.deploymentEnvironment">deploymentEnvironment</a></code> | <code>string</code> | *No description.* |
| <code><a href="#cdk-constructs.DeployConfig.property.deploymentSitename">deploymentSitename</a></code> | <code>string</code> | *No description.* |
| <code><a href="#cdk-constructs.DeployConfig.property.projectId">projectId</a></code> | <code>string</code> | *No description.* |

---

##### `deploymentAwsAccount`<sup>Required</sup> <a name="deploymentAwsAccount" id="cdk-constructs.DeployConfig.property.deploymentAwsAccount"></a>

```typescript
public readonly deploymentAwsAccount: string;
```

- *Type:* string

---

##### `deploymentAwsRegion`<sup>Required</sup> <a name="deploymentAwsRegion" id="cdk-constructs.DeployConfig.property.deploymentAwsRegion"></a>

```typescript
public readonly deploymentAwsRegion: string;
```

- *Type:* string

---

##### `deploymentEnvironment`<sup>Required</sup> <a name="deploymentEnvironment" id="cdk-constructs.DeployConfig.property.deploymentEnvironment"></a>

```typescript
public readonly deploymentEnvironment: string;
```

- *Type:* string

---

##### `deploymentSitename`<sup>Required</sup> <a name="deploymentSitename" id="cdk-constructs.DeployConfig.property.deploymentSitename"></a>

```typescript
public readonly deploymentSitename: string;
```

- *Type:* string

---

##### `projectId`<sup>Required</sup> <a name="projectId" id="cdk-constructs.DeployConfig.property.projectId"></a>

```typescript
public readonly projectId: string;
```

- *Type:* string

---

### DeployStepConf <a name="DeployStepConf" id="cdk-constructs.DeployStepConf"></a>

#### Initializer <a name="Initializer" id="cdk-constructs.DeployStepConf.Initializer"></a>

```typescript
import { DeployStepConf } from 'cdk-constructs'

const deployStepConf: DeployStepConf = { ... }
```

#### Properties <a name="Properties" id="Properties"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.DeployStepConf.property.computeType">computeType</a></code> | <code>aws-cdk-lib.aws_codebuild.ComputeType</code> | Specify the size of the build containers. See https://docs.aws.amazon.com/codebuild/latest/userguide/build-env-ref-compute-types.html#environment.types for reference. |
| <code><a href="#cdk-constructs.DeployStepConf.property.customBuildImage">customBuildImage</a></code> | <code>aws-cdk-lib.aws_codebuild.IBuildImage</code> | Build image to be used fot this step. |
| <code><a href="#cdk-constructs.DeployStepConf.property.environmentalVariables">environmentalVariables</a></code> | <code>{[ key: string ]: aws-cdk-lib.aws_codebuild.BuildEnvironmentVariable}</code> | Map of additional env vars to pass to the build container. |
| <code><a href="#cdk-constructs.DeployStepConf.property.environmentConf">environmentConf</a></code> | <code><a href="#cdk-constructs.DeployConfig">DeployConfig</a></code> | *No description.* |

---

##### `computeType`<sup>Optional</sup> <a name="computeType" id="cdk-constructs.DeployStepConf.property.computeType"></a>

```typescript
public readonly computeType: ComputeType;
```

- *Type:* aws-cdk-lib.aws_codebuild.ComputeType

Specify the size of the build containers. See https://docs.aws.amazon.com/codebuild/latest/userguide/build-env-ref-compute-types.html#environment.types for reference.

Defaults to `ComputeType.SMALL`

---

##### `customBuildImage`<sup>Optional</sup> <a name="customBuildImage" id="cdk-constructs.DeployStepConf.property.customBuildImage"></a>

```typescript
public readonly customBuildImage: IBuildImage;
```

- *Type:* aws-cdk-lib.aws_codebuild.IBuildImage

Build image to be used fot this step.

---

##### `environmentalVariables`<sup>Optional</sup> <a name="environmentalVariables" id="cdk-constructs.DeployStepConf.property.environmentalVariables"></a>

```typescript
public readonly environmentalVariables: {[ key: string ]: BuildEnvironmentVariable};
```

- *Type:* {[ key: string ]: aws-cdk-lib.aws_codebuild.BuildEnvironmentVariable}

Map of additional env vars to pass to the build container.

---

##### `environmentConf`<sup>Required</sup> <a name="environmentConf" id="cdk-constructs.DeployStepConf.property.environmentConf"></a>

```typescript
public readonly environmentConf: DeployConfig;
```

- *Type:* <a href="#cdk-constructs.DeployConfig">DeployConfig</a>

---

### ECRDeploymentProps <a name="ECRDeploymentProps" id="cdk-constructs.ECRDeploymentProps"></a>

#### Initializer <a name="Initializer" id="cdk-constructs.ECRDeploymentProps.Initializer"></a>

```typescript
import { ECRDeploymentProps } from 'cdk-constructs'

const eCRDeploymentProps: ECRDeploymentProps = { ... }
```

#### Properties <a name="Properties" id="Properties"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.ECRDeploymentProps.property.dest">dest</a></code> | <code><a href="#cdk-constructs.IImageName">IImageName</a></code> | The destination of the docker image. |
| <code><a href="#cdk-constructs.ECRDeploymentProps.property.src">src</a></code> | <code><a href="#cdk-constructs.IImageName">IImageName</a></code> | The source of the docker image. |
| <code><a href="#cdk-constructs.ECRDeploymentProps.property.buildImage">buildImage</a></code> | <code>string</code> | Image to use to build Golang lambda for custom resource, if download fails or is not wanted. |
| <code><a href="#cdk-constructs.ECRDeploymentProps.property.environment">environment</a></code> | <code>{[ key: string ]: string}</code> | The environment variable to set. |
| <code><a href="#cdk-constructs.ECRDeploymentProps.property.memoryLimit">memoryLimit</a></code> | <code>number</code> | The amount of memory (in MiB) to allocate to the AWS Lambda function which replicates the files from the CDK bucket to the destination bucket. |
| <code><a href="#cdk-constructs.ECRDeploymentProps.property.role">role</a></code> | <code>aws-cdk-lib.aws_iam.IRole</code> | Execution role associated with this function. |
| <code><a href="#cdk-constructs.ECRDeploymentProps.property.vpc">vpc</a></code> | <code>aws-cdk-lib.aws_ec2.IVpc</code> | The VPC network to place the deployment lambda handler in. |
| <code><a href="#cdk-constructs.ECRDeploymentProps.property.vpcSubnets">vpcSubnets</a></code> | <code>aws-cdk-lib.aws_ec2.SubnetSelection</code> | Where in the VPC to place the deployment lambda handler. |

---

##### `dest`<sup>Required</sup> <a name="dest" id="cdk-constructs.ECRDeploymentProps.property.dest"></a>

```typescript
public readonly dest: IImageName;
```

- *Type:* <a href="#cdk-constructs.IImageName">IImageName</a>

The destination of the docker image.

---

##### `src`<sup>Required</sup> <a name="src" id="cdk-constructs.ECRDeploymentProps.property.src"></a>

```typescript
public readonly src: IImageName;
```

- *Type:* <a href="#cdk-constructs.IImageName">IImageName</a>

The source of the docker image.

---

##### `buildImage`<sup>Optional</sup> <a name="buildImage" id="cdk-constructs.ECRDeploymentProps.property.buildImage"></a>

```typescript
public readonly buildImage: string;
```

- *Type:* string
- *Default:* public.ecr.aws/sam/build-go1.x:latest

Image to use to build Golang lambda for custom resource, if download fails or is not wanted.

Might be needed for local build if all images need to come from own registry.

Note that image should use yum as a package manager and have golang available.

---

##### `environment`<sup>Optional</sup> <a name="environment" id="cdk-constructs.ECRDeploymentProps.property.environment"></a>

```typescript
public readonly environment: {[ key: string ]: string};
```

- *Type:* {[ key: string ]: string}

The environment variable to set.

---

##### `memoryLimit`<sup>Optional</sup> <a name="memoryLimit" id="cdk-constructs.ECRDeploymentProps.property.memoryLimit"></a>

```typescript
public readonly memoryLimit: number;
```

- *Type:* number
- *Default:* 512

The amount of memory (in MiB) to allocate to the AWS Lambda function which replicates the files from the CDK bucket to the destination bucket.

If you are deploying large files, you will need to increase this number
accordingly.

---

##### `role`<sup>Optional</sup> <a name="role" id="cdk-constructs.ECRDeploymentProps.property.role"></a>

```typescript
public readonly role: IRole;
```

- *Type:* aws-cdk-lib.aws_iam.IRole
- *Default:* A role is automatically created

Execution role associated with this function.

---

##### `vpc`<sup>Optional</sup> <a name="vpc" id="cdk-constructs.ECRDeploymentProps.property.vpc"></a>

```typescript
public readonly vpc: IVpc;
```

- *Type:* aws-cdk-lib.aws_ec2.IVpc
- *Default:* None

The VPC network to place the deployment lambda handler in.

---

##### `vpcSubnets`<sup>Optional</sup> <a name="vpcSubnets" id="cdk-constructs.ECRDeploymentProps.property.vpcSubnets"></a>

```typescript
public readonly vpcSubnets: SubnetSelection;
```

- *Type:* aws-cdk-lib.aws_ec2.SubnetSelection
- *Default:* the Vpc default strategy if not specified

Where in the VPC to place the deployment lambda handler.

Only used if 'vpc' is supplied.

---

### EndpointComponents <a name="EndpointComponents" id="cdk-constructs.EndpointComponents"></a>

#### Initializer <a name="Initializer" id="cdk-constructs.EndpointComponents.Initializer"></a>

```typescript
import { EndpointComponents } from 'cdk-constructs'

const endpointComponents: EndpointComponents = { ... }
```

#### Properties <a name="Properties" id="Properties"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.EndpointComponents.property.domain">domain</a></code> | <code>string</code> | The domain part of the endpoint, i.e. `awsd04-product-api-adv1-productimports.4me.cdndev.weebo.it`. |
| <code><a href="#cdk-constructs.EndpointComponents.property.fullRecord">fullRecord</a></code> | <code>string</code> | The full endpoint record, i.e. `awsd04-product-api-adv1-productimports.4me.cdndev.weebo.it/api/adv1/productimports/`. |
| <code><a href="#cdk-constructs.EndpointComponents.property.path">path</a></code> | <code>string</code> | The path of the endpoint, i.e. `/api/adv1/productimports/`. |

---

##### `domain`<sup>Required</sup> <a name="domain" id="cdk-constructs.EndpointComponents.property.domain"></a>

```typescript
public readonly domain: string;
```

- *Type:* string

The domain part of the endpoint, i.e. `awsd04-product-api-adv1-productimports.4me.cdndev.weebo.it`.

---

##### `fullRecord`<sup>Required</sup> <a name="fullRecord" id="cdk-constructs.EndpointComponents.property.fullRecord"></a>

```typescript
public readonly fullRecord: string;
```

- *Type:* string

The full endpoint record, i.e. `awsd04-product-api-adv1-productimports.4me.cdndev.weebo.it/api/adv1/productimports/`.

---

##### `path`<sup>Required</sup> <a name="path" id="cdk-constructs.EndpointComponents.property.path"></a>

```typescript
public readonly path: string;
```

- *Type:* string

The path of the endpoint, i.e. `/api/adv1/productimports/`.

---

### EnvironmentConfig <a name="EnvironmentConfig" id="cdk-constructs.EnvironmentConfig"></a>

#### Initializer <a name="Initializer" id="cdk-constructs.EnvironmentConfig.Initializer"></a>

```typescript
import { EnvironmentConfig } from 'cdk-constructs'

const environmentConfig: EnvironmentConfig = { ... }
```

#### Properties <a name="Properties" id="Properties"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.EnvironmentConfig.property.deploymentAwsAccount">deploymentAwsAccount</a></code> | <code>string</code> | *No description.* |
| <code><a href="#cdk-constructs.EnvironmentConfig.property.deploymentAwsRegion">deploymentAwsRegion</a></code> | <code>string</code> | *No description.* |
| <code><a href="#cdk-constructs.EnvironmentConfig.property.deploymentEnvironment">deploymentEnvironment</a></code> | <code>string</code> | *No description.* |
| <code><a href="#cdk-constructs.EnvironmentConfig.property.deploymentSitename">deploymentSitename</a></code> | <code>string</code> | *No description.* |

---

##### `deploymentAwsAccount`<sup>Required</sup> <a name="deploymentAwsAccount" id="cdk-constructs.EnvironmentConfig.property.deploymentAwsAccount"></a>

```typescript
public readonly deploymentAwsAccount: string;
```

- *Type:* string

---

##### `deploymentAwsRegion`<sup>Required</sup> <a name="deploymentAwsRegion" id="cdk-constructs.EnvironmentConfig.property.deploymentAwsRegion"></a>

```typescript
public readonly deploymentAwsRegion: string;
```

- *Type:* string

---

##### `deploymentEnvironment`<sup>Required</sup> <a name="deploymentEnvironment" id="cdk-constructs.EnvironmentConfig.property.deploymentEnvironment"></a>

```typescript
public readonly deploymentEnvironment: string;
```

- *Type:* string

---

##### `deploymentSitename`<sup>Required</sup> <a name="deploymentSitename" id="cdk-constructs.EnvironmentConfig.property.deploymentSitename"></a>

```typescript
public readonly deploymentSitename: string;
```

- *Type:* string

---

### FullServiceProps <a name="FullServiceProps" id="cdk-constructs.FullServiceProps"></a>

#### Initializer <a name="Initializer" id="cdk-constructs.FullServiceProps.Initializer"></a>

```typescript
import { FullServiceProps } from 'cdk-constructs'

const fullServiceProps: FullServiceProps = { ... }
```

#### Properties <a name="Properties" id="Properties"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.FullServiceProps.property.serviceGroup">serviceGroup</a></code> | <code><a href="#cdk-constructs.ServiceGroup">ServiceGroup</a></code> | Service group of the service. |
| <code><a href="#cdk-constructs.FullServiceProps.property.version">version</a></code> | <code>number</code> | The version of the API exposed by the endpoint. |
| <code><a href="#cdk-constructs.FullServiceProps.property.visibility">visibility</a></code> | <code><a href="#cdk-constructs.EndpointVisibility">EndpointVisibility</a></code> | Wether the endpoint is private or public. |
| <code><a href="#cdk-constructs.FullServiceProps.property.serviceName">serviceName</a></code> | <code>string</code> | Name of the service the endpoint exposes. |

---

##### `serviceGroup`<sup>Required</sup> <a name="serviceGroup" id="cdk-constructs.FullServiceProps.property.serviceGroup"></a>

```typescript
public readonly serviceGroup: ServiceGroup;
```

- *Type:* <a href="#cdk-constructs.ServiceGroup">ServiceGroup</a>
- *Default:* ServiceGroup.VIEW

Service group of the service.

---

##### `version`<sup>Required</sup> <a name="version" id="cdk-constructs.FullServiceProps.property.version"></a>

```typescript
public readonly version: number;
```

- *Type:* number
- *Default:* 1

The version of the API exposed by the endpoint.

---

##### `visibility`<sup>Required</sup> <a name="visibility" id="cdk-constructs.FullServiceProps.property.visibility"></a>

```typescript
public readonly visibility: EndpointVisibility;
```

- *Type:* <a href="#cdk-constructs.EndpointVisibility">EndpointVisibility</a>
- *Default:* EndpointVisibility.PRIVATE

Wether the endpoint is private or public.

---

##### `serviceName`<sup>Required</sup> <a name="serviceName" id="cdk-constructs.FullServiceProps.property.serviceName"></a>

```typescript
public readonly serviceName: string;
```

- *Type:* string

Name of the service the endpoint exposes.

---

### FunctionOptions <a name="FunctionOptions" id="cdk-constructs.FunctionOptions"></a>

#### Initializer <a name="Initializer" id="cdk-constructs.FunctionOptions.Initializer"></a>

```typescript
import { FunctionOptions } from 'cdk-constructs'

const functionOptions: FunctionOptions = { ... }
```

#### Properties <a name="Properties" id="Properties"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.FunctionOptions.property.apiGatewayEndpoints">apiGatewayEndpoints</a></code> | <code>{[ key: string ]: <a href="#cdk-constructs.ThronLambdaApiGatewayEndpointProps">ThronLambdaApiGatewayEndpointProps</a>}</code> | Api Gateway endpoints associated with this lambda. |
| <code><a href="#cdk-constructs.FunctionOptions.property.architecture">architecture</a></code> | <code>aws-cdk-lib.aws_lambda.Architecture</code> | The architecture the lambda function runs on. |
| <code><a href="#cdk-constructs.FunctionOptions.property.areMultiValueHeadersEnabled">areMultiValueHeadersEnabled</a></code> | <code>boolean</code> | Whether or not multi value headers are enabled. |
| <code><a href="#cdk-constructs.FunctionOptions.property.description">description</a></code> | <code>string</code> | A description of the function. |
| <code><a href="#cdk-constructs.FunctionOptions.property.dockerContextPath">dockerContextPath</a></code> | <code>string</code> | Context of docker build. |
| <code><a href="#cdk-constructs.FunctionOptions.property.dockerfileName">dockerfileName</a></code> | <code>string</code> | Name of Dockerfile. |
| <code><a href="#cdk-constructs.FunctionOptions.property.endpoints">endpoints</a></code> | <code>{[ key: string ]: <a href="#cdk-constructs.ThronEndpointAlbProps">ThronEndpointAlbProps</a>}</code> | Endpoints associated with this lambda. |
| <code><a href="#cdk-constructs.FunctionOptions.property.environment">environment</a></code> | <code>{[ key: string ]: string}</code> | Key-value pairs that Lambda caches and makes available for your Lambda functions. |
| <code><a href="#cdk-constructs.FunctionOptions.property.ephemeralStorageSize">ephemeralStorageSize</a></code> | <code>aws-cdk-lib.Size</code> | The size of the function’s /tmp directory in MiB. |
| <code><a href="#cdk-constructs.FunctionOptions.property.existingDockerImage">existingDockerImage</a></code> | <code>aws-cdk-lib.aws_lambda.DockerImageCode</code> | Existing docker image. |
| <code><a href="#cdk-constructs.FunctionOptions.property.filesystem">filesystem</a></code> | <code>aws-cdk-lib.aws_lambda.FileSystem</code> | The filesystem configuration for the lambda function. |
| <code><a href="#cdk-constructs.FunctionOptions.property.legacyEndpoints">legacyEndpoints</a></code> | <code>{[ key: string ]: <a href="#cdk-constructs.LegacyEndpointAlbProps">LegacyEndpointAlbProps</a>}</code> | Legacy endpoints associated with this lambda. |
| <code><a href="#cdk-constructs.FunctionOptions.property.memorySize">memorySize</a></code> | <code>number</code> | The amount of memory, in MB, that is allocated to your Lambda function. |
| <code><a href="#cdk-constructs.FunctionOptions.property.reservedConcurrentExecutions">reservedConcurrentExecutions</a></code> | <code>number</code> | The maximum of concurrent executions you want to reserve for the function. |
| <code><a href="#cdk-constructs.FunctionOptions.property.timeout">timeout</a></code> | <code>aws-cdk-lib.Duration</code> | The function execution time (in seconds) after which Lambda terminates the function. |

---

##### `apiGatewayEndpoints`<sup>Optional</sup> <a name="apiGatewayEndpoints" id="cdk-constructs.FunctionOptions.property.apiGatewayEndpoints"></a>

```typescript
public readonly apiGatewayEndpoints: {[ key: string ]: ThronLambdaApiGatewayEndpointProps};
```

- *Type:* {[ key: string ]: <a href="#cdk-constructs.ThronLambdaApiGatewayEndpointProps">ThronLambdaApiGatewayEndpointProps</a>}

Api Gateway endpoints associated with this lambda.

---

##### `architecture`<sup>Optional</sup> <a name="architecture" id="cdk-constructs.FunctionOptions.property.architecture"></a>

```typescript
public readonly architecture: Architecture;
```

- *Type:* aws-cdk-lib.aws_lambda.Architecture
- *Default:* lambda.Architecture.X86_64

The architecture the lambda function runs on.

---

##### `areMultiValueHeadersEnabled`<sup>Optional</sup> <a name="areMultiValueHeadersEnabled" id="cdk-constructs.FunctionOptions.property.areMultiValueHeadersEnabled"></a>

```typescript
public readonly areMultiValueHeadersEnabled: boolean;
```

- *Type:* boolean
- *Default:* false

Whether or not multi value headers are enabled.

If you enable this flag may need to made some slight modification; more info at the following link
https://docs.aws.amazon.com/elasticloadbalancing/latest/application/lambda-functions.html#multi-value-headers

---

##### `description`<sup>Optional</sup> <a name="description" id="cdk-constructs.FunctionOptions.property.description"></a>

```typescript
public readonly description: string;
```

- *Type:* string
- *Default:* No description.

A description of the function.

---

##### `dockerContextPath`<sup>Optional</sup> <a name="dockerContextPath" id="cdk-constructs.FunctionOptions.property.dockerContextPath"></a>

```typescript
public readonly dockerContextPath: string;
```

- *Type:* string

Context of docker build.

---

##### `dockerfileName`<sup>Optional</sup> <a name="dockerfileName" id="cdk-constructs.FunctionOptions.property.dockerfileName"></a>

```typescript
public readonly dockerfileName: string;
```

- *Type:* string
- *Default:* Dockerfile

Name of Dockerfile.

---

##### `endpoints`<sup>Optional</sup> <a name="endpoints" id="cdk-constructs.FunctionOptions.property.endpoints"></a>

```typescript
public readonly endpoints: {[ key: string ]: ThronEndpointAlbProps};
```

- *Type:* {[ key: string ]: <a href="#cdk-constructs.ThronEndpointAlbProps">ThronEndpointAlbProps</a>}

Endpoints associated with this lambda.

---

##### `environment`<sup>Optional</sup> <a name="environment" id="cdk-constructs.FunctionOptions.property.environment"></a>

```typescript
public readonly environment: {[ key: string ]: string};
```

- *Type:* {[ key: string ]: string}
- *Default:* No environment variables.

Key-value pairs that Lambda caches and makes available for your Lambda functions.

Use environment variables to apply configuration changes, such
as test and production environment configurations, without changing your
Lambda function source code.

---

##### `ephemeralStorageSize`<sup>Optional</sup> <a name="ephemeralStorageSize" id="cdk-constructs.FunctionOptions.property.ephemeralStorageSize"></a>

```typescript
public readonly ephemeralStorageSize: Size;
```

- *Type:* aws-cdk-lib.Size
- *Default:* 512 MiB

The size of the function’s /tmp directory in MiB.

---

##### `existingDockerImage`<sup>Optional</sup> <a name="existingDockerImage" id="cdk-constructs.FunctionOptions.property.existingDockerImage"></a>

```typescript
public readonly existingDockerImage: DockerImageCode;
```

- *Type:* aws-cdk-lib.aws_lambda.DockerImageCode

Existing docker image.

---

##### `filesystem`<sup>Optional</sup> <a name="filesystem" id="cdk-constructs.FunctionOptions.property.filesystem"></a>

```typescript
public readonly filesystem: FileSystem;
```

- *Type:* aws-cdk-lib.aws_lambda.FileSystem
- *Default:* will not mount any filesystem

The filesystem configuration for the lambda function.

---

##### `legacyEndpoints`<sup>Optional</sup> <a name="legacyEndpoints" id="cdk-constructs.FunctionOptions.property.legacyEndpoints"></a>

```typescript
public readonly legacyEndpoints: {[ key: string ]: LegacyEndpointAlbProps};
```

- *Type:* {[ key: string ]: <a href="#cdk-constructs.LegacyEndpointAlbProps">LegacyEndpointAlbProps</a>}

Legacy endpoints associated with this lambda.

---

##### `memorySize`<sup>Optional</sup> <a name="memorySize" id="cdk-constructs.FunctionOptions.property.memorySize"></a>

```typescript
public readonly memorySize: number;
```

- *Type:* number
- *Default:* 128

The amount of memory, in MB, that is allocated to your Lambda function.

Lambda uses this value to proportionally allocate the amount of CPU
power. For more information, see Resource Model in the AWS Lambda
Developer Guide.

---

##### `reservedConcurrentExecutions`<sup>Optional</sup> <a name="reservedConcurrentExecutions" id="cdk-constructs.FunctionOptions.property.reservedConcurrentExecutions"></a>

```typescript
public readonly reservedConcurrentExecutions: number;
```

- *Type:* number
- *Default:* No specific limit - account limit.

The maximum of concurrent executions you want to reserve for the function.

---

##### `timeout`<sup>Optional</sup> <a name="timeout" id="cdk-constructs.FunctionOptions.property.timeout"></a>

```typescript
public readonly timeout: Duration;
```

- *Type:* aws-cdk-lib.Duration
- *Default:* Duration.seconds(3)

The function execution time (in seconds) after which Lambda terminates the function.

Because the execution time affects cost, set this value
based on the function's expected execution time.

---

### LambdaConf <a name="LambdaConf" id="cdk-constructs.LambdaConf"></a>

#### Initializer <a name="Initializer" id="cdk-constructs.LambdaConf.Initializer"></a>

```typescript
import { LambdaConf } from 'cdk-constructs'

const lambdaConf: LambdaConf = { ... }
```

#### Properties <a name="Properties" id="Properties"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.LambdaConf.property.computeType">computeType</a></code> | <code>aws-cdk-lib.aws_codebuild.ComputeType</code> | Specify the size of the build containers. See https://docs.aws.amazon.com/codebuild/latest/userguide/build-env-ref-compute-types.html#environment.types for reference. |
| <code><a href="#cdk-constructs.LambdaConf.property.customBuildImage">customBuildImage</a></code> | <code>aws-cdk-lib.aws_codebuild.IBuildImage</code> | Build image to be used fot this step. |
| <code><a href="#cdk-constructs.LambdaConf.property.environmentalVariables">environmentalVariables</a></code> | <code>{[ key: string ]: aws-cdk-lib.aws_codebuild.BuildEnvironmentVariable}</code> | Map of additional env vars to pass to the build container. |
| <code><a href="#cdk-constructs.LambdaConf.property.destinationEcrRepository">destinationEcrRepository</a></code> | <code>aws-cdk-lib.aws_ecr.Repository</code> | *No description.* |

---

##### `computeType`<sup>Optional</sup> <a name="computeType" id="cdk-constructs.LambdaConf.property.computeType"></a>

```typescript
public readonly computeType: ComputeType;
```

- *Type:* aws-cdk-lib.aws_codebuild.ComputeType

Specify the size of the build containers. See https://docs.aws.amazon.com/codebuild/latest/userguide/build-env-ref-compute-types.html#environment.types for reference.

Defaults to `ComputeType.SMALL`

---

##### `customBuildImage`<sup>Optional</sup> <a name="customBuildImage" id="cdk-constructs.LambdaConf.property.customBuildImage"></a>

```typescript
public readonly customBuildImage: IBuildImage;
```

- *Type:* aws-cdk-lib.aws_codebuild.IBuildImage

Build image to be used fot this step.

---

##### `environmentalVariables`<sup>Optional</sup> <a name="environmentalVariables" id="cdk-constructs.LambdaConf.property.environmentalVariables"></a>

```typescript
public readonly environmentalVariables: {[ key: string ]: BuildEnvironmentVariable};
```

- *Type:* {[ key: string ]: aws-cdk-lib.aws_codebuild.BuildEnvironmentVariable}

Map of additional env vars to pass to the build container.

---

##### `destinationEcrRepository`<sup>Required</sup> <a name="destinationEcrRepository" id="cdk-constructs.LambdaConf.property.destinationEcrRepository"></a>

```typescript
public readonly destinationEcrRepository: Repository;
```

- *Type:* aws-cdk-lib.aws_ecr.Repository

---

### LegacyEndpointAlbProps <a name="LegacyEndpointAlbProps" id="cdk-constructs.LegacyEndpointAlbProps"></a>

#### Initializer <a name="Initializer" id="cdk-constructs.LegacyEndpointAlbProps.Initializer"></a>

```typescript
import { LegacyEndpointAlbProps } from 'cdk-constructs'

const legacyEndpointAlbProps: LegacyEndpointAlbProps = { ... }
```

#### Properties <a name="Properties" id="Properties"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.LegacyEndpointAlbProps.property.routingTokenPrefix">routingTokenPrefix</a></code> | <code>string</code> | Routing path for the service, validated against `serviceGroup`. |
| <code><a href="#cdk-constructs.LegacyEndpointAlbProps.property.serviceGroup">serviceGroup</a></code> | <code><a href="#cdk-constructs.ServiceGroup">ServiceGroup</a></code> | Service group of the service. |
| <code><a href="#cdk-constructs.LegacyEndpointAlbProps.property.deleteExistingDns">deleteExistingDns</a></code> | <code>boolean</code> | DANGEROUS: Overwrite dns record if it already exists, otherwise it creates it. |
| <code><a href="#cdk-constructs.LegacyEndpointAlbProps.property.stack">stack</a></code> | <code>aws-cdk-lib.Stack</code> | The reference of parent Stack. |

---

##### `routingTokenPrefix`<sup>Required</sup> <a name="routingTokenPrefix" id="cdk-constructs.LegacyEndpointAlbProps.property.routingTokenPrefix"></a>

```typescript
public readonly routingTokenPrefix: string;
```

- *Type:* string

Routing path for the service, validated against `serviceGroup`.

---

##### `serviceGroup`<sup>Required</sup> <a name="serviceGroup" id="cdk-constructs.LegacyEndpointAlbProps.property.serviceGroup"></a>

```typescript
public readonly serviceGroup: ServiceGroup;
```

- *Type:* <a href="#cdk-constructs.ServiceGroup">ServiceGroup</a>

Service group of the service.

---

##### `deleteExistingDns`<sup>Optional</sup> <a name="deleteExistingDns" id="cdk-constructs.LegacyEndpointAlbProps.property.deleteExistingDns"></a>

```typescript
public readonly deleteExistingDns: boolean;
```

- *Type:* boolean
- *Default:* false

DANGEROUS: Overwrite dns record if it already exists, otherwise it creates it.

---

##### `stack`<sup>Optional</sup> <a name="stack" id="cdk-constructs.LegacyEndpointAlbProps.property.stack"></a>

```typescript
public readonly stack: Stack;
```

- *Type:* aws-cdk-lib.Stack

The reference of parent Stack.

---

### NewRelicFunctionOptions <a name="NewRelicFunctionOptions" id="cdk-constructs.NewRelicFunctionOptions"></a>

#### Initializer <a name="Initializer" id="cdk-constructs.NewRelicFunctionOptions.Initializer"></a>

```typescript
import { NewRelicFunctionOptions } from 'cdk-constructs'

const newRelicFunctionOptions: NewRelicFunctionOptions = { ... }
```

#### Properties <a name="Properties" id="Properties"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.NewRelicFunctionOptions.property.apiGatewayEndpoints">apiGatewayEndpoints</a></code> | <code>{[ key: string ]: <a href="#cdk-constructs.ThronLambdaApiGatewayEndpointProps">ThronLambdaApiGatewayEndpointProps</a>}</code> | Api Gateway endpoints associated with this lambda. |
| <code><a href="#cdk-constructs.NewRelicFunctionOptions.property.architecture">architecture</a></code> | <code>aws-cdk-lib.aws_lambda.Architecture</code> | The architecture the lambda function runs on. |
| <code><a href="#cdk-constructs.NewRelicFunctionOptions.property.areMultiValueHeadersEnabled">areMultiValueHeadersEnabled</a></code> | <code>boolean</code> | Whether or not multi value headers are enabled. |
| <code><a href="#cdk-constructs.NewRelicFunctionOptions.property.description">description</a></code> | <code>string</code> | A description of the function. |
| <code><a href="#cdk-constructs.NewRelicFunctionOptions.property.dockerContextPath">dockerContextPath</a></code> | <code>string</code> | Context of docker build. |
| <code><a href="#cdk-constructs.NewRelicFunctionOptions.property.dockerfileName">dockerfileName</a></code> | <code>string</code> | Name of Dockerfile. |
| <code><a href="#cdk-constructs.NewRelicFunctionOptions.property.endpoints">endpoints</a></code> | <code>{[ key: string ]: <a href="#cdk-constructs.ThronEndpointAlbProps">ThronEndpointAlbProps</a>}</code> | Endpoints associated with this lambda. |
| <code><a href="#cdk-constructs.NewRelicFunctionOptions.property.environment">environment</a></code> | <code>{[ key: string ]: string}</code> | Key-value pairs that Lambda caches and makes available for your Lambda functions. |
| <code><a href="#cdk-constructs.NewRelicFunctionOptions.property.ephemeralStorageSize">ephemeralStorageSize</a></code> | <code>aws-cdk-lib.Size</code> | The size of the function’s /tmp directory in MiB. |
| <code><a href="#cdk-constructs.NewRelicFunctionOptions.property.existingDockerImage">existingDockerImage</a></code> | <code>aws-cdk-lib.aws_lambda.DockerImageCode</code> | Existing docker image. |
| <code><a href="#cdk-constructs.NewRelicFunctionOptions.property.filesystem">filesystem</a></code> | <code>aws-cdk-lib.aws_lambda.FileSystem</code> | The filesystem configuration for the lambda function. |
| <code><a href="#cdk-constructs.NewRelicFunctionOptions.property.legacyEndpoints">legacyEndpoints</a></code> | <code>{[ key: string ]: <a href="#cdk-constructs.LegacyEndpointAlbProps">LegacyEndpointAlbProps</a>}</code> | Legacy endpoints associated with this lambda. |
| <code><a href="#cdk-constructs.NewRelicFunctionOptions.property.memorySize">memorySize</a></code> | <code>number</code> | The amount of memory, in MB, that is allocated to your Lambda function. |
| <code><a href="#cdk-constructs.NewRelicFunctionOptions.property.reservedConcurrentExecutions">reservedConcurrentExecutions</a></code> | <code>number</code> | The maximum of concurrent executions you want to reserve for the function. |
| <code><a href="#cdk-constructs.NewRelicFunctionOptions.property.timeout">timeout</a></code> | <code>aws-cdk-lib.Duration</code> | The function execution time (in seconds) after which Lambda terminates the function. |
| <code><a href="#cdk-constructs.NewRelicFunctionOptions.property.newRelicConfigOverrides">newRelicConfigOverrides</a></code> | <code><a href="#cdk-constructs.NewRelicLambdaConfigOverrides">NewRelicLambdaConfigOverrides</a></code> | Explicit Overrides for NewRelic Configuration. |

---

##### `apiGatewayEndpoints`<sup>Optional</sup> <a name="apiGatewayEndpoints" id="cdk-constructs.NewRelicFunctionOptions.property.apiGatewayEndpoints"></a>

```typescript
public readonly apiGatewayEndpoints: {[ key: string ]: ThronLambdaApiGatewayEndpointProps};
```

- *Type:* {[ key: string ]: <a href="#cdk-constructs.ThronLambdaApiGatewayEndpointProps">ThronLambdaApiGatewayEndpointProps</a>}

Api Gateway endpoints associated with this lambda.

---

##### `architecture`<sup>Optional</sup> <a name="architecture" id="cdk-constructs.NewRelicFunctionOptions.property.architecture"></a>

```typescript
public readonly architecture: Architecture;
```

- *Type:* aws-cdk-lib.aws_lambda.Architecture
- *Default:* lambda.Architecture.X86_64

The architecture the lambda function runs on.

---

##### `areMultiValueHeadersEnabled`<sup>Optional</sup> <a name="areMultiValueHeadersEnabled" id="cdk-constructs.NewRelicFunctionOptions.property.areMultiValueHeadersEnabled"></a>

```typescript
public readonly areMultiValueHeadersEnabled: boolean;
```

- *Type:* boolean
- *Default:* false

Whether or not multi value headers are enabled.

If you enable this flag may need to made some slight modification; more info at the following link
https://docs.aws.amazon.com/elasticloadbalancing/latest/application/lambda-functions.html#multi-value-headers

---

##### `description`<sup>Optional</sup> <a name="description" id="cdk-constructs.NewRelicFunctionOptions.property.description"></a>

```typescript
public readonly description: string;
```

- *Type:* string
- *Default:* No description.

A description of the function.

---

##### `dockerContextPath`<sup>Optional</sup> <a name="dockerContextPath" id="cdk-constructs.NewRelicFunctionOptions.property.dockerContextPath"></a>

```typescript
public readonly dockerContextPath: string;
```

- *Type:* string

Context of docker build.

---

##### `dockerfileName`<sup>Optional</sup> <a name="dockerfileName" id="cdk-constructs.NewRelicFunctionOptions.property.dockerfileName"></a>

```typescript
public readonly dockerfileName: string;
```

- *Type:* string
- *Default:* Dockerfile

Name of Dockerfile.

---

##### `endpoints`<sup>Optional</sup> <a name="endpoints" id="cdk-constructs.NewRelicFunctionOptions.property.endpoints"></a>

```typescript
public readonly endpoints: {[ key: string ]: ThronEndpointAlbProps};
```

- *Type:* {[ key: string ]: <a href="#cdk-constructs.ThronEndpointAlbProps">ThronEndpointAlbProps</a>}

Endpoints associated with this lambda.

---

##### `environment`<sup>Optional</sup> <a name="environment" id="cdk-constructs.NewRelicFunctionOptions.property.environment"></a>

```typescript
public readonly environment: {[ key: string ]: string};
```

- *Type:* {[ key: string ]: string}
- *Default:* No environment variables.

Key-value pairs that Lambda caches and makes available for your Lambda functions.

Use environment variables to apply configuration changes, such
as test and production environment configurations, without changing your
Lambda function source code.

---

##### `ephemeralStorageSize`<sup>Optional</sup> <a name="ephemeralStorageSize" id="cdk-constructs.NewRelicFunctionOptions.property.ephemeralStorageSize"></a>

```typescript
public readonly ephemeralStorageSize: Size;
```

- *Type:* aws-cdk-lib.Size
- *Default:* 512 MiB

The size of the function’s /tmp directory in MiB.

---

##### `existingDockerImage`<sup>Optional</sup> <a name="existingDockerImage" id="cdk-constructs.NewRelicFunctionOptions.property.existingDockerImage"></a>

```typescript
public readonly existingDockerImage: DockerImageCode;
```

- *Type:* aws-cdk-lib.aws_lambda.DockerImageCode

Existing docker image.

---

##### `filesystem`<sup>Optional</sup> <a name="filesystem" id="cdk-constructs.NewRelicFunctionOptions.property.filesystem"></a>

```typescript
public readonly filesystem: FileSystem;
```

- *Type:* aws-cdk-lib.aws_lambda.FileSystem
- *Default:* will not mount any filesystem

The filesystem configuration for the lambda function.

---

##### `legacyEndpoints`<sup>Optional</sup> <a name="legacyEndpoints" id="cdk-constructs.NewRelicFunctionOptions.property.legacyEndpoints"></a>

```typescript
public readonly legacyEndpoints: {[ key: string ]: LegacyEndpointAlbProps};
```

- *Type:* {[ key: string ]: <a href="#cdk-constructs.LegacyEndpointAlbProps">LegacyEndpointAlbProps</a>}

Legacy endpoints associated with this lambda.

---

##### `memorySize`<sup>Optional</sup> <a name="memorySize" id="cdk-constructs.NewRelicFunctionOptions.property.memorySize"></a>

```typescript
public readonly memorySize: number;
```

- *Type:* number
- *Default:* 128

The amount of memory, in MB, that is allocated to your Lambda function.

Lambda uses this value to proportionally allocate the amount of CPU
power. For more information, see Resource Model in the AWS Lambda
Developer Guide.

---

##### `reservedConcurrentExecutions`<sup>Optional</sup> <a name="reservedConcurrentExecutions" id="cdk-constructs.NewRelicFunctionOptions.property.reservedConcurrentExecutions"></a>

```typescript
public readonly reservedConcurrentExecutions: number;
```

- *Type:* number
- *Default:* No specific limit - account limit.

The maximum of concurrent executions you want to reserve for the function.

---

##### `timeout`<sup>Optional</sup> <a name="timeout" id="cdk-constructs.NewRelicFunctionOptions.property.timeout"></a>

```typescript
public readonly timeout: Duration;
```

- *Type:* aws-cdk-lib.Duration
- *Default:* Duration.seconds(3)

The function execution time (in seconds) after which Lambda terminates the function.

Because the execution time affects cost, set this value
based on the function's expected execution time.

---

##### `newRelicConfigOverrides`<sup>Optional</sup> <a name="newRelicConfigOverrides" id="cdk-constructs.NewRelicFunctionOptions.property.newRelicConfigOverrides"></a>

```typescript
public readonly newRelicConfigOverrides: NewRelicLambdaConfigOverrides;
```

- *Type:* <a href="#cdk-constructs.NewRelicLambdaConfigOverrides">NewRelicLambdaConfigOverrides</a>
- *Default:* Empty object with no overrides

Explicit Overrides for NewRelic Configuration.

---

### NewRelicLambdaConfig <a name="NewRelicLambdaConfig" id="cdk-constructs.NewRelicLambdaConfig"></a>

#### Initializer <a name="Initializer" id="cdk-constructs.NewRelicLambdaConfig.Initializer"></a>

```typescript
import { NewRelicLambdaConfig } from 'cdk-constructs'

const newRelicLambdaConfig: NewRelicLambdaConfig = { ... }
```

#### Properties <a name="Properties" id="Properties"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.NewRelicLambdaConfig.property.newRelicAccountId">newRelicAccountId</a></code> | <code>string</code> | *No description.* |
| <code><a href="#cdk-constructs.NewRelicLambdaConfig.property.newRelicDistributedTracingEnabled">newRelicDistributedTracingEnabled</a></code> | <code>boolean</code> | *No description.* |
| <code><a href="#cdk-constructs.NewRelicLambdaConfig.property.newRelicExtensionLogsEnabled">newRelicExtensionLogsEnabled</a></code> | <code>boolean</code> | *No description.* |
| <code><a href="#cdk-constructs.NewRelicLambdaConfig.property.newRelicExtensionSendFunctionLogs">newRelicExtensionSendFunctionLogs</a></code> | <code>boolean</code> | *No description.* |
| <code><a href="#cdk-constructs.NewRelicLambdaConfig.property.newRelicIgnoreExtensionChecks">newRelicIgnoreExtensionChecks</a></code> | <code><a href="#cdk-constructs.NewRelicIgnoreExtensionChecksOption">NewRelicIgnoreExtensionChecksOption</a>[]</code> | *No description.* |
| <code><a href="#cdk-constructs.NewRelicLambdaConfig.property.newRelicLambdaExtensionEnabled">newRelicLambdaExtensionEnabled</a></code> | <code>boolean</code> | *No description.* |
| <code><a href="#cdk-constructs.NewRelicLambdaConfig.property.newRelicLicenseKey">newRelicLicenseKey</a></code> | <code>string</code> | *No description.* |
| <code><a href="#cdk-constructs.NewRelicLambdaConfig.property.newRelicLicenseKeyParameterName">newRelicLicenseKeyParameterName</a></code> | <code>string</code> | *No description.* |
| <code><a href="#cdk-constructs.NewRelicLambdaConfig.property.newRelicTrustedAccountKey">newRelicTrustedAccountKey</a></code> | <code>string</code> | *No description.* |

---

##### `newRelicAccountId`<sup>Required</sup> <a name="newRelicAccountId" id="cdk-constructs.NewRelicLambdaConfig.property.newRelicAccountId"></a>

```typescript
public readonly newRelicAccountId: string;
```

- *Type:* string

---

##### `newRelicDistributedTracingEnabled`<sup>Required</sup> <a name="newRelicDistributedTracingEnabled" id="cdk-constructs.NewRelicLambdaConfig.property.newRelicDistributedTracingEnabled"></a>

```typescript
public readonly newRelicDistributedTracingEnabled: boolean;
```

- *Type:* boolean

---

##### `newRelicExtensionLogsEnabled`<sup>Required</sup> <a name="newRelicExtensionLogsEnabled" id="cdk-constructs.NewRelicLambdaConfig.property.newRelicExtensionLogsEnabled"></a>

```typescript
public readonly newRelicExtensionLogsEnabled: boolean;
```

- *Type:* boolean

---

##### `newRelicExtensionSendFunctionLogs`<sup>Required</sup> <a name="newRelicExtensionSendFunctionLogs" id="cdk-constructs.NewRelicLambdaConfig.property.newRelicExtensionSendFunctionLogs"></a>

```typescript
public readonly newRelicExtensionSendFunctionLogs: boolean;
```

- *Type:* boolean

---

##### `newRelicIgnoreExtensionChecks`<sup>Required</sup> <a name="newRelicIgnoreExtensionChecks" id="cdk-constructs.NewRelicLambdaConfig.property.newRelicIgnoreExtensionChecks"></a>

```typescript
public readonly newRelicIgnoreExtensionChecks: NewRelicIgnoreExtensionChecksOption[];
```

- *Type:* <a href="#cdk-constructs.NewRelicIgnoreExtensionChecksOption">NewRelicIgnoreExtensionChecksOption</a>[]

---

##### `newRelicLambdaExtensionEnabled`<sup>Required</sup> <a name="newRelicLambdaExtensionEnabled" id="cdk-constructs.NewRelicLambdaConfig.property.newRelicLambdaExtensionEnabled"></a>

```typescript
public readonly newRelicLambdaExtensionEnabled: boolean;
```

- *Type:* boolean

---

##### `newRelicLicenseKey`<sup>Required</sup> <a name="newRelicLicenseKey" id="cdk-constructs.NewRelicLambdaConfig.property.newRelicLicenseKey"></a>

```typescript
public readonly newRelicLicenseKey: string;
```

- *Type:* string

---

##### `newRelicLicenseKeyParameterName`<sup>Required</sup> <a name="newRelicLicenseKeyParameterName" id="cdk-constructs.NewRelicLambdaConfig.property.newRelicLicenseKeyParameterName"></a>

```typescript
public readonly newRelicLicenseKeyParameterName: string;
```

- *Type:* string

---

##### `newRelicTrustedAccountKey`<sup>Required</sup> <a name="newRelicTrustedAccountKey" id="cdk-constructs.NewRelicLambdaConfig.property.newRelicTrustedAccountKey"></a>

```typescript
public readonly newRelicTrustedAccountKey: string;
```

- *Type:* string

---

### NewRelicLambdaConfigOverrides <a name="NewRelicLambdaConfigOverrides" id="cdk-constructs.NewRelicLambdaConfigOverrides"></a>

#### Initializer <a name="Initializer" id="cdk-constructs.NewRelicLambdaConfigOverrides.Initializer"></a>

```typescript
import { NewRelicLambdaConfigOverrides } from 'cdk-constructs'

const newRelicLambdaConfigOverrides: NewRelicLambdaConfigOverrides = { ... }
```

#### Properties <a name="Properties" id="Properties"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.NewRelicLambdaConfigOverrides.property.newRelicAccountId">newRelicAccountId</a></code> | <code>string</code> | *No description.* |
| <code><a href="#cdk-constructs.NewRelicLambdaConfigOverrides.property.newRelicDistributedTracingEnabled">newRelicDistributedTracingEnabled</a></code> | <code>boolean</code> | *No description.* |
| <code><a href="#cdk-constructs.NewRelicLambdaConfigOverrides.property.newRelicExtensionLogsEnabled">newRelicExtensionLogsEnabled</a></code> | <code>boolean</code> | *No description.* |
| <code><a href="#cdk-constructs.NewRelicLambdaConfigOverrides.property.newRelicExtensionSendFunctionLogs">newRelicExtensionSendFunctionLogs</a></code> | <code>boolean</code> | *No description.* |
| <code><a href="#cdk-constructs.NewRelicLambdaConfigOverrides.property.newRelicIgnoreExtensionChecks">newRelicIgnoreExtensionChecks</a></code> | <code><a href="#cdk-constructs.NewRelicIgnoreExtensionChecksOption">NewRelicIgnoreExtensionChecksOption</a>[]</code> | *No description.* |
| <code><a href="#cdk-constructs.NewRelicLambdaConfigOverrides.property.newRelicLambdaExtensionEnabled">newRelicLambdaExtensionEnabled</a></code> | <code>boolean</code> | *No description.* |
| <code><a href="#cdk-constructs.NewRelicLambdaConfigOverrides.property.newRelicLicenseKey">newRelicLicenseKey</a></code> | <code>string</code> | *No description.* |
| <code><a href="#cdk-constructs.NewRelicLambdaConfigOverrides.property.newRelicLicenseKeyParameterName">newRelicLicenseKeyParameterName</a></code> | <code>string</code> | *No description.* |
| <code><a href="#cdk-constructs.NewRelicLambdaConfigOverrides.property.newRelicTrustedAccountKey">newRelicTrustedAccountKey</a></code> | <code>string</code> | *No description.* |

---

##### `newRelicAccountId`<sup>Optional</sup> <a name="newRelicAccountId" id="cdk-constructs.NewRelicLambdaConfigOverrides.property.newRelicAccountId"></a>

```typescript
public readonly newRelicAccountId: string;
```

- *Type:* string

---

##### `newRelicDistributedTracingEnabled`<sup>Optional</sup> <a name="newRelicDistributedTracingEnabled" id="cdk-constructs.NewRelicLambdaConfigOverrides.property.newRelicDistributedTracingEnabled"></a>

```typescript
public readonly newRelicDistributedTracingEnabled: boolean;
```

- *Type:* boolean

---

##### `newRelicExtensionLogsEnabled`<sup>Optional</sup> <a name="newRelicExtensionLogsEnabled" id="cdk-constructs.NewRelicLambdaConfigOverrides.property.newRelicExtensionLogsEnabled"></a>

```typescript
public readonly newRelicExtensionLogsEnabled: boolean;
```

- *Type:* boolean

---

##### `newRelicExtensionSendFunctionLogs`<sup>Optional</sup> <a name="newRelicExtensionSendFunctionLogs" id="cdk-constructs.NewRelicLambdaConfigOverrides.property.newRelicExtensionSendFunctionLogs"></a>

```typescript
public readonly newRelicExtensionSendFunctionLogs: boolean;
```

- *Type:* boolean

---

##### `newRelicIgnoreExtensionChecks`<sup>Optional</sup> <a name="newRelicIgnoreExtensionChecks" id="cdk-constructs.NewRelicLambdaConfigOverrides.property.newRelicIgnoreExtensionChecks"></a>

```typescript
public readonly newRelicIgnoreExtensionChecks: NewRelicIgnoreExtensionChecksOption[];
```

- *Type:* <a href="#cdk-constructs.NewRelicIgnoreExtensionChecksOption">NewRelicIgnoreExtensionChecksOption</a>[]

---

##### `newRelicLambdaExtensionEnabled`<sup>Optional</sup> <a name="newRelicLambdaExtensionEnabled" id="cdk-constructs.NewRelicLambdaConfigOverrides.property.newRelicLambdaExtensionEnabled"></a>

```typescript
public readonly newRelicLambdaExtensionEnabled: boolean;
```

- *Type:* boolean

---

##### `newRelicLicenseKey`<sup>Optional</sup> <a name="newRelicLicenseKey" id="cdk-constructs.NewRelicLambdaConfigOverrides.property.newRelicLicenseKey"></a>

```typescript
public readonly newRelicLicenseKey: string;
```

- *Type:* string

---

##### `newRelicLicenseKeyParameterName`<sup>Optional</sup> <a name="newRelicLicenseKeyParameterName" id="cdk-constructs.NewRelicLambdaConfigOverrides.property.newRelicLicenseKeyParameterName"></a>

```typescript
public readonly newRelicLicenseKeyParameterName: string;
```

- *Type:* string

---

##### `newRelicTrustedAccountKey`<sup>Optional</sup> <a name="newRelicTrustedAccountKey" id="cdk-constructs.NewRelicLambdaConfigOverrides.property.newRelicTrustedAccountKey"></a>

```typescript
public readonly newRelicTrustedAccountKey: string;
```

- *Type:* string

---

### NotifyConf <a name="NotifyConf" id="cdk-constructs.NotifyConf"></a>

Configuration for the notifier webhook.

#### Initializer <a name="Initializer" id="cdk-constructs.NotifyConf.Initializer"></a>

```typescript
import { NotifyConf } from 'cdk-constructs'

const notifyConf: NotifyConf = { ... }
```

#### Properties <a name="Properties" id="Properties"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.NotifyConf.property.notifyCapabilities">notifyCapabilities</a></code> | <code><a href="#cdk-constructs.PipelineCapability">PipelineCapability</a>[]</code> | List of capabilities for notification purposes. |
| <code><a href="#cdk-constructs.NotifyConf.property.webhookUrl">webhookUrl</a></code> | <code>string</code> | Ms Teams webhook url to send the notifications to. |

---

##### `notifyCapabilities`<sup>Required</sup> <a name="notifyCapabilities" id="cdk-constructs.NotifyConf.property.notifyCapabilities"></a>

```typescript
public readonly notifyCapabilities: PipelineCapability[];
```

- *Type:* <a href="#cdk-constructs.PipelineCapability">PipelineCapability</a>[]

List of capabilities for notification purposes.

All of them must start with `NOTIFY_ON`

---

##### `webhookUrl`<sup>Required</sup> <a name="webhookUrl" id="cdk-constructs.NotifyConf.property.webhookUrl"></a>

```typescript
public readonly webhookUrl: string;
```

- *Type:* string

Ms Teams webhook url to send the notifications to.

---

### NotifyLambdaEnv <a name="NotifyLambdaEnv" id="cdk-constructs.NotifyLambdaEnv"></a>

#### Initializer <a name="Initializer" id="cdk-constructs.NotifyLambdaEnv.Initializer"></a>

```typescript
import { NotifyLambdaEnv } from 'cdk-constructs'

const notifyLambdaEnv: NotifyLambdaEnv = { ... }
```

#### Properties <a name="Properties" id="Properties"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.NotifyLambdaEnv.property.branch">branch</a></code> | <code>string</code> | *No description.* |
| <code><a href="#cdk-constructs.NotifyLambdaEnv.property.env">env</a></code> | <code>string</code> | *No description.* |
| <code><a href="#cdk-constructs.NotifyLambdaEnv.property.projectId">projectId</a></code> | <code>string</code> | *No description.* |
| <code><a href="#cdk-constructs.NotifyLambdaEnv.property.repository">repository</a></code> | <code>string</code> | *No description.* |
| <code><a href="#cdk-constructs.NotifyLambdaEnv.property.webhookUrl">webhookUrl</a></code> | <code>string</code> | *No description.* |

---

##### `branch`<sup>Required</sup> <a name="branch" id="cdk-constructs.NotifyLambdaEnv.property.branch"></a>

```typescript
public readonly branch: string;
```

- *Type:* string

---

##### `env`<sup>Required</sup> <a name="env" id="cdk-constructs.NotifyLambdaEnv.property.env"></a>

```typescript
public readonly env: string;
```

- *Type:* string

---

##### `projectId`<sup>Required</sup> <a name="projectId" id="cdk-constructs.NotifyLambdaEnv.property.projectId"></a>

```typescript
public readonly projectId: string;
```

- *Type:* string

---

##### `repository`<sup>Required</sup> <a name="repository" id="cdk-constructs.NotifyLambdaEnv.property.repository"></a>

```typescript
public readonly repository: string;
```

- *Type:* string

---

##### `webhookUrl`<sup>Required</sup> <a name="webhookUrl" id="cdk-constructs.NotifyLambdaEnv.property.webhookUrl"></a>

```typescript
public readonly webhookUrl: string;
```

- *Type:* string

---

### OptionalServiceProps <a name="OptionalServiceProps" id="cdk-constructs.OptionalServiceProps"></a>

#### Initializer <a name="Initializer" id="cdk-constructs.OptionalServiceProps.Initializer"></a>

```typescript
import { OptionalServiceProps } from 'cdk-constructs'

const optionalServiceProps: OptionalServiceProps = { ... }
```

#### Properties <a name="Properties" id="Properties"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.OptionalServiceProps.property.serviceGroup">serviceGroup</a></code> | <code><a href="#cdk-constructs.ServiceGroup">ServiceGroup</a></code> | Service group of the service. |
| <code><a href="#cdk-constructs.OptionalServiceProps.property.version">version</a></code> | <code>number</code> | The version of the API exposed by the endpoint. |
| <code><a href="#cdk-constructs.OptionalServiceProps.property.visibility">visibility</a></code> | <code><a href="#cdk-constructs.EndpointVisibility">EndpointVisibility</a></code> | Wether the endpoint is private or public. |

---

##### `serviceGroup`<sup>Required</sup> <a name="serviceGroup" id="cdk-constructs.OptionalServiceProps.property.serviceGroup"></a>

```typescript
public readonly serviceGroup: ServiceGroup;
```

- *Type:* <a href="#cdk-constructs.ServiceGroup">ServiceGroup</a>
- *Default:* ServiceGroup.VIEW

Service group of the service.

---

##### `version`<sup>Required</sup> <a name="version" id="cdk-constructs.OptionalServiceProps.property.version"></a>

```typescript
public readonly version: number;
```

- *Type:* number
- *Default:* 1

The version of the API exposed by the endpoint.

---

##### `visibility`<sup>Required</sup> <a name="visibility" id="cdk-constructs.OptionalServiceProps.property.visibility"></a>

```typescript
public readonly visibility: EndpointVisibility;
```

- *Type:* <a href="#cdk-constructs.EndpointVisibility">EndpointVisibility</a>
- *Default:* EndpointVisibility.PRIVATE

Wether the endpoint is private or public.

---

### OptionalServicePropsPartial <a name="OptionalServicePropsPartial" id="cdk-constructs.OptionalServicePropsPartial"></a>

#### Initializer <a name="Initializer" id="cdk-constructs.OptionalServicePropsPartial.Initializer"></a>

```typescript
import { OptionalServicePropsPartial } from 'cdk-constructs'

const optionalServicePropsPartial: OptionalServicePropsPartial = { ... }
```

#### Properties <a name="Properties" id="Properties"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.OptionalServicePropsPartial.property.serviceGroup">serviceGroup</a></code> | <code><a href="#cdk-constructs.ServiceGroup">ServiceGroup</a></code> | Service group of the service. |
| <code><a href="#cdk-constructs.OptionalServicePropsPartial.property.version">version</a></code> | <code>number</code> | The version of the API exposed by the endpoint. |
| <code><a href="#cdk-constructs.OptionalServicePropsPartial.property.visibility">visibility</a></code> | <code><a href="#cdk-constructs.EndpointVisibility">EndpointVisibility</a></code> | Wether the endpoint is private or public. |

---

##### `serviceGroup`<sup>Optional</sup> <a name="serviceGroup" id="cdk-constructs.OptionalServicePropsPartial.property.serviceGroup"></a>

```typescript
public readonly serviceGroup: ServiceGroup;
```

- *Type:* <a href="#cdk-constructs.ServiceGroup">ServiceGroup</a>
- *Default:* ServiceGroup.VIEW

Service group of the service.

---

##### `version`<sup>Optional</sup> <a name="version" id="cdk-constructs.OptionalServicePropsPartial.property.version"></a>

```typescript
public readonly version: number;
```

- *Type:* number
- *Default:* 1

The version of the API exposed by the endpoint.

---

##### `visibility`<sup>Optional</sup> <a name="visibility" id="cdk-constructs.OptionalServicePropsPartial.property.visibility"></a>

```typescript
public readonly visibility: EndpointVisibility;
```

- *Type:* <a href="#cdk-constructs.EndpointVisibility">EndpointVisibility</a>
- *Default:* EndpointVisibility.PRIVATE

Wether the endpoint is private or public.

---

### OtherAccountPeeringConfig <a name="OtherAccountPeeringConfig" id="cdk-constructs.OtherAccountPeeringConfig"></a>

#### Initializer <a name="Initializer" id="cdk-constructs.OtherAccountPeeringConfig.Initializer"></a>

```typescript
import { OtherAccountPeeringConfig } from 'cdk-constructs'

const otherAccountPeeringConfig: OtherAccountPeeringConfig = { ... }
```

#### Properties <a name="Properties" id="Properties"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.OtherAccountPeeringConfig.property.otherVpcAccountId">otherVpcAccountId</a></code> | <code>string</code> | VPC to be peered account's ID. |
| <code><a href="#cdk-constructs.OtherAccountPeeringConfig.property.otherVpcCidr">otherVpcCidr</a></code> | <code>string</code> | VPC to be peered mnemonic Id. |
| <code><a href="#cdk-constructs.OtherAccountPeeringConfig.property.otherVpcId">otherVpcId</a></code> | <code>string</code> | VPC to be peered vpcId. |
| <code><a href="#cdk-constructs.OtherAccountPeeringConfig.property.otherVpcRegion">otherVpcRegion</a></code> | <code>string</code> | VPC to be peered region. |
| <code><a href="#cdk-constructs.OtherAccountPeeringConfig.property.uniquePeeringId">uniquePeeringId</a></code> | <code>string</code> | VPC to be peered mnemonic Id. |

---

##### `otherVpcAccountId`<sup>Required</sup> <a name="otherVpcAccountId" id="cdk-constructs.OtherAccountPeeringConfig.property.otherVpcAccountId"></a>

```typescript
public readonly otherVpcAccountId: string;
```

- *Type:* string

VPC to be peered account's ID.

---

##### `otherVpcCidr`<sup>Required</sup> <a name="otherVpcCidr" id="cdk-constructs.OtherAccountPeeringConfig.property.otherVpcCidr"></a>

```typescript
public readonly otherVpcCidr: string;
```

- *Type:* string

VPC to be peered mnemonic Id.

---

##### `otherVpcId`<sup>Required</sup> <a name="otherVpcId" id="cdk-constructs.OtherAccountPeeringConfig.property.otherVpcId"></a>

```typescript
public readonly otherVpcId: string;
```

- *Type:* string

VPC to be peered vpcId.

---

##### `otherVpcRegion`<sup>Required</sup> <a name="otherVpcRegion" id="cdk-constructs.OtherAccountPeeringConfig.property.otherVpcRegion"></a>

```typescript
public readonly otherVpcRegion: string;
```

- *Type:* string

VPC to be peered region.

---

##### `uniquePeeringId`<sup>Required</sup> <a name="uniquePeeringId" id="cdk-constructs.OtherAccountPeeringConfig.property.uniquePeeringId"></a>

```typescript
public readonly uniquePeeringId: string;
```

- *Type:* string

VPC to be peered mnemonic Id.

---

### PeeringConfig <a name="PeeringConfig" id="cdk-constructs.PeeringConfig"></a>

Route to add to the route tables, pointing to an already paired VPC.

#### Initializer <a name="Initializer" id="cdk-constructs.PeeringConfig.Initializer"></a>

```typescript
import { PeeringConfig } from 'cdk-constructs'

const peeringConfig: PeeringConfig = { ... }
```

#### Properties <a name="Properties" id="Properties"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.PeeringConfig.property.otherVpc">otherVpc</a></code> | <code>aws-cdk-lib.aws_ec2.IVpc</code> | Id of vpc peering. |
| <code><a href="#cdk-constructs.PeeringConfig.property.peeringId">peeringId</a></code> | <code>string</code> | Unique id for this route. |

---

##### `otherVpc`<sup>Required</sup> <a name="otherVpc" id="cdk-constructs.PeeringConfig.property.otherVpc"></a>

```typescript
public readonly otherVpc: IVpc;
```

- *Type:* aws-cdk-lib.aws_ec2.IVpc

Id of vpc peering.

---

##### `peeringId`<sup>Required</sup> <a name="peeringId" id="cdk-constructs.PeeringConfig.property.peeringId"></a>

```typescript
public readonly peeringId: string;
```

- *Type:* string

Unique id for this route.

---

### ProjectPreset <a name="ProjectPreset" id="cdk-constructs.ProjectPreset"></a>

#### Initializer <a name="Initializer" id="cdk-constructs.ProjectPreset.Initializer"></a>

```typescript
import { ProjectPreset } from 'cdk-constructs'

const projectPreset: ProjectPreset = { ... }
```

#### Properties <a name="Properties" id="Properties"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.ProjectPreset.property.repositoryBranchTagOrSha">repositoryBranchTagOrSha</a></code> | <code>string</code> | *No description.* |
| <code><a href="#cdk-constructs.ProjectPreset.property.repositoryName">repositoryName</a></code> | <code>string</code> | *No description.* |
| <code><a href="#cdk-constructs.ProjectPreset.property.repositoryRegion">repositoryRegion</a></code> | <code>string</code> | *No description.* |
| <code><a href="#cdk-constructs.ProjectPreset.property.subConfigs">subConfigs</a></code> | <code><a href="#cdk-constructs.ProjectSubConfig">ProjectSubConfig</a>[]</code> | *No description.* |

---

##### `repositoryBranchTagOrSha`<sup>Required</sup> <a name="repositoryBranchTagOrSha" id="cdk-constructs.ProjectPreset.property.repositoryBranchTagOrSha"></a>

```typescript
public readonly repositoryBranchTagOrSha: string;
```

- *Type:* string

---

##### `repositoryName`<sup>Required</sup> <a name="repositoryName" id="cdk-constructs.ProjectPreset.property.repositoryName"></a>

```typescript
public readonly repositoryName: string;
```

- *Type:* string

---

##### `repositoryRegion`<sup>Required</sup> <a name="repositoryRegion" id="cdk-constructs.ProjectPreset.property.repositoryRegion"></a>

```typescript
public readonly repositoryRegion: string;
```

- *Type:* string

---

##### `subConfigs`<sup>Required</sup> <a name="subConfigs" id="cdk-constructs.ProjectPreset.property.subConfigs"></a>

```typescript
public readonly subConfigs: ProjectSubConfig[];
```

- *Type:* <a href="#cdk-constructs.ProjectSubConfig">ProjectSubConfig</a>[]

---

### ProjectSubConfig <a name="ProjectSubConfig" id="cdk-constructs.ProjectSubConfig"></a>

#### Initializer <a name="Initializer" id="cdk-constructs.ProjectSubConfig.Initializer"></a>

```typescript
import { ProjectSubConfig } from 'cdk-constructs'

const projectSubConfig: ProjectSubConfig = { ... }
```

#### Properties <a name="Properties" id="Properties"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.ProjectSubConfig.property.replaceValue">replaceValue</a></code> | <code>string</code> | *No description.* |
| <code><a href="#cdk-constructs.ProjectSubConfig.property.searchValue">searchValue</a></code> | <code>string</code> | *No description.* |

---

##### `replaceValue`<sup>Required</sup> <a name="replaceValue" id="cdk-constructs.ProjectSubConfig.property.replaceValue"></a>

```typescript
public readonly replaceValue: string;
```

- *Type:* string

---

##### `searchValue`<sup>Required</sup> <a name="searchValue" id="cdk-constructs.ProjectSubConfig.property.searchValue"></a>

```typescript
public readonly searchValue: string;
```

- *Type:* string

---

### SsmParameterReaderProps <a name="SsmParameterReaderProps" id="cdk-constructs.SsmParameterReaderProps"></a>

SSMParameter Reader Configuration.

#### Initializer <a name="Initializer" id="cdk-constructs.SsmParameterReaderProps.Initializer"></a>

```typescript
import { SsmParameterReaderProps } from 'cdk-constructs'

const ssmParameterReaderProps: SsmParameterReaderProps = { ... }
```

#### Properties <a name="Properties" id="Properties"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.SsmParameterReaderProps.property.parameterName">parameterName</a></code> | <code>string</code> | Complete name of the ssm parameter you want to read. |

---

##### `parameterName`<sup>Required</sup> <a name="parameterName" id="cdk-constructs.SsmParameterReaderProps.property.parameterName"></a>

```typescript
public readonly parameterName: string;
```

- *Type:* string

Complete name of the ssm parameter you want to read.

---

### StageProducts <a name="StageProducts" id="cdk-constructs.StageProducts"></a>

#### Initializer <a name="Initializer" id="cdk-constructs.StageProducts.Initializer"></a>

```typescript
import { StageProducts } from 'cdk-constructs'

const stageProducts: StageProducts = { ... }
```

#### Properties <a name="Properties" id="Properties"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.StageProducts.property.actions">actions</a></code> | <code>aws-cdk-lib.aws_codepipeline_actions.Action[]</code> | *No description.* |
| <code><a href="#cdk-constructs.StageProducts.property.buildProjects">buildProjects</a></code> | <code><a href="#cdk-constructs.ThronPipelineBuildProject">ThronPipelineBuildProject</a>[]</code> | *No description.* |
| <code><a href="#cdk-constructs.StageProducts.property.name">name</a></code> | <code>string</code> | *No description.* |

---

##### `actions`<sup>Required</sup> <a name="actions" id="cdk-constructs.StageProducts.property.actions"></a>

```typescript
public readonly actions: Action[];
```

- *Type:* aws-cdk-lib.aws_codepipeline_actions.Action[]

---

##### `buildProjects`<sup>Required</sup> <a name="buildProjects" id="cdk-constructs.StageProducts.property.buildProjects"></a>

```typescript
public readonly buildProjects: ThronPipelineBuildProject[];
```

- *Type:* <a href="#cdk-constructs.ThronPipelineBuildProject">ThronPipelineBuildProject</a>[]

---

##### `name`<sup>Required</sup> <a name="name" id="cdk-constructs.StageProducts.property.name"></a>

```typescript
public readonly name: string;
```

- *Type:* string

---

### StepConfig <a name="StepConfig" id="cdk-constructs.StepConfig"></a>

Custom overrides for each single action in the pipeline.

#### Initializer <a name="Initializer" id="cdk-constructs.StepConfig.Initializer"></a>

```typescript
import { StepConfig } from 'cdk-constructs'

const stepConfig: StepConfig = { ... }
```

#### Properties <a name="Properties" id="Properties"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.StepConfig.property.computeType">computeType</a></code> | <code>aws-cdk-lib.aws_codebuild.ComputeType</code> | Specify the size of the build containers. See https://docs.aws.amazon.com/codebuild/latest/userguide/build-env-ref-compute-types.html#environment.types for reference. |
| <code><a href="#cdk-constructs.StepConfig.property.customBuildImage">customBuildImage</a></code> | <code>aws-cdk-lib.aws_codebuild.IBuildImage</code> | Build image to be used fot this step. |
| <code><a href="#cdk-constructs.StepConfig.property.environmentalVariables">environmentalVariables</a></code> | <code>{[ key: string ]: aws-cdk-lib.aws_codebuild.BuildEnvironmentVariable}</code> | Map of additional env vars to pass to the build container. |

---

##### `computeType`<sup>Optional</sup> <a name="computeType" id="cdk-constructs.StepConfig.property.computeType"></a>

```typescript
public readonly computeType: ComputeType;
```

- *Type:* aws-cdk-lib.aws_codebuild.ComputeType

Specify the size of the build containers. See https://docs.aws.amazon.com/codebuild/latest/userguide/build-env-ref-compute-types.html#environment.types for reference.

Defaults to `ComputeType.SMALL`

---

##### `customBuildImage`<sup>Optional</sup> <a name="customBuildImage" id="cdk-constructs.StepConfig.property.customBuildImage"></a>

```typescript
public readonly customBuildImage: IBuildImage;
```

- *Type:* aws-cdk-lib.aws_codebuild.IBuildImage

Build image to be used fot this step.

---

##### `environmentalVariables`<sup>Optional</sup> <a name="environmentalVariables" id="cdk-constructs.StepConfig.property.environmentalVariables"></a>

```typescript
public readonly environmentalVariables: {[ key: string ]: BuildEnvironmentVariable};
```

- *Type:* {[ key: string ]: aws-cdk-lib.aws_codebuild.BuildEnvironmentVariable}

Map of additional env vars to pass to the build container.

---

### SubnetConfigProps <a name="SubnetConfigProps" id="cdk-constructs.SubnetConfigProps"></a>

Configuration to create a new subnet.

#### Initializer <a name="Initializer" id="cdk-constructs.SubnetConfigProps.Initializer"></a>

```typescript
import { SubnetConfigProps } from 'cdk-constructs'

const subnetConfigProps: SubnetConfigProps = { ... }
```

#### Properties <a name="Properties" id="Properties"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.SubnetConfigProps.property.availabilityZone">availabilityZone</a></code> | <code><a href="#cdk-constructs.AvailabilityZone">AvailabilityZone</a></code> | The AZ in which to place the subnet. |
| <code><a href="#cdk-constructs.SubnetConfigProps.property.ipv4Cidr">ipv4Cidr</a></code> | <code>string</code> | The ipv4 CIDR block to be assigned to this subnet. |
| <code><a href="#cdk-constructs.SubnetConfigProps.property.ipv6CidrSlotNumber">ipv6CidrSlotNumber</a></code> | <code>number</code> | The ipv6 CIDR block to assigned to this subnet (1-255). |
| <code><a href="#cdk-constructs.SubnetConfigProps.property.type">type</a></code> | <code><a href="#cdk-constructs.SubnetType">SubnetType</a></code> | Whether the subnet is public or private. |

---

##### `availabilityZone`<sup>Required</sup> <a name="availabilityZone" id="cdk-constructs.SubnetConfigProps.property.availabilityZone"></a>

```typescript
public readonly availabilityZone: AvailabilityZone;
```

- *Type:* <a href="#cdk-constructs.AvailabilityZone">AvailabilityZone</a>

The AZ in which to place the subnet.

---

##### `ipv4Cidr`<sup>Required</sup> <a name="ipv4Cidr" id="cdk-constructs.SubnetConfigProps.property.ipv4Cidr"></a>

```typescript
public readonly ipv4Cidr: string;
```

- *Type:* string

The ipv4 CIDR block to be assigned to this subnet.

---

##### `ipv6CidrSlotNumber`<sup>Required</sup> <a name="ipv6CidrSlotNumber" id="cdk-constructs.SubnetConfigProps.property.ipv6CidrSlotNumber"></a>

```typescript
public readonly ipv6CidrSlotNumber: number;
```

- *Type:* number

The ipv6 CIDR block to assigned to this subnet (1-255).

The assigned slot is a /64 by convention

The assigned slot is derived from the automatically assigned /56 VPC CIDR block.

---

##### `type`<sup>Required</sup> <a name="type" id="cdk-constructs.SubnetConfigProps.property.type"></a>

```typescript
public readonly type: SubnetType;
```

- *Type:* <a href="#cdk-constructs.SubnetType">SubnetType</a>

Whether the subnet is public or private.

---

### ThronAcmCertificateProps <a name="ThronAcmCertificateProps" id="cdk-constructs.ThronAcmCertificateProps"></a>

#### Initializer <a name="Initializer" id="cdk-constructs.ThronAcmCertificateProps.Initializer"></a>

```typescript
import { ThronAcmCertificateProps } from 'cdk-constructs'

const thronAcmCertificateProps: ThronAcmCertificateProps = { ... }
```

#### Properties <a name="Properties" id="Properties"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.ThronAcmCertificateProps.property.domainName">domainName</a></code> | <code>string</code> | FQDN to issue the certificate for. |
| <code><a href="#cdk-constructs.ThronAcmCertificateProps.property.region">region</a></code> | <code>string</code> | Region where to create the certificate, defaults to main stack region. |
| <code><a href="#cdk-constructs.ThronAcmCertificateProps.property.subjectAlternativeNames">subjectAlternativeNames</a></code> | <code>string[]</code> | Alternative domain names on the certificate. |

---

##### `domainName`<sup>Required</sup> <a name="domainName" id="cdk-constructs.ThronAcmCertificateProps.property.domainName"></a>

```typescript
public readonly domainName: string;
```

- *Type:* string

FQDN to issue the certificate for.

---

##### `region`<sup>Optional</sup> <a name="region" id="cdk-constructs.ThronAcmCertificateProps.property.region"></a>

```typescript
public readonly region: string;
```

- *Type:* string

Region where to create the certificate, defaults to main stack region.

---

##### `subjectAlternativeNames`<sup>Optional</sup> <a name="subjectAlternativeNames" id="cdk-constructs.ThronAcmCertificateProps.property.subjectAlternativeNames"></a>

```typescript
public readonly subjectAlternativeNames: string[];
```

- *Type:* string[]

Alternative domain names on the certificate.

---

### ThronApiGatewayApiProps <a name="ThronApiGatewayApiProps" id="cdk-constructs.ThronApiGatewayApiProps"></a>

#### Initializer <a name="Initializer" id="cdk-constructs.ThronApiGatewayApiProps.Initializer"></a>

```typescript
import { ThronApiGatewayApiProps } from 'cdk-constructs'

const thronApiGatewayApiProps: ThronApiGatewayApiProps = { ... }
```

#### Properties <a name="Properties" id="Properties"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.ThronApiGatewayApiProps.property.mainDomain">mainDomain</a></code> | <code>string</code> | The main domain of the api gateway api, **without the cdn part**. |

---

##### `mainDomain`<sup>Required</sup> <a name="mainDomain" id="cdk-constructs.ThronApiGatewayApiProps.property.mainDomain"></a>

```typescript
public readonly mainDomain: string;
```

- *Type:* string

The main domain of the api gateway api, **without the cdn part**.

I.e `awsd04-product-api-adv1-productimports`

---

### ThronApiGatewayDomainAliasProps <a name="ThronApiGatewayDomainAliasProps" id="cdk-constructs.ThronApiGatewayDomainAliasProps"></a>

Properties to instantiate a new ThronDomainAlias.

#### Initializer <a name="Initializer" id="cdk-constructs.ThronApiGatewayDomainAliasProps.Initializer"></a>

```typescript
import { ThronApiGatewayDomainAliasProps } from 'cdk-constructs'

const thronApiGatewayDomainAliasProps: ThronApiGatewayDomainAliasProps = { ... }
```

#### Properties <a name="Properties" id="Properties"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.ThronApiGatewayDomainAliasProps.property.apiGatewayApi">apiGatewayApi</a></code> | <code>aws-cdk-lib.aws_apigateway.IRestApi</code> | API to create the alias to. |
| <code><a href="#cdk-constructs.ThronApiGatewayDomainAliasProps.property.domainName">domainName</a></code> | <code>string</code> | Domain name to alias the API Gateway Endpoint to. |
| <code><a href="#cdk-constructs.ThronApiGatewayDomainAliasProps.property.prefix">prefix</a></code> | <code>string</code> | Unique id to add to CFN ids to prevent the first synth from failing. |

---

##### `apiGatewayApi`<sup>Required</sup> <a name="apiGatewayApi" id="cdk-constructs.ThronApiGatewayDomainAliasProps.property.apiGatewayApi"></a>

```typescript
public readonly apiGatewayApi: IRestApi;
```

- *Type:* aws-cdk-lib.aws_apigateway.IRestApi

API to create the alias to.

---

##### `domainName`<sup>Required</sup> <a name="domainName" id="cdk-constructs.ThronApiGatewayDomainAliasProps.property.domainName"></a>

```typescript
public readonly domainName: string;
```

- *Type:* string

Domain name to alias the API Gateway Endpoint to.

---

##### `prefix`<sup>Required</sup> <a name="prefix" id="cdk-constructs.ThronApiGatewayDomainAliasProps.property.prefix"></a>

```typescript
public readonly prefix: string;
```

- *Type:* string

Unique id to add to CFN ids to prevent the first synth from failing.

---

### ThronCachePolicyProps <a name="ThronCachePolicyProps" id="cdk-constructs.ThronCachePolicyProps"></a>

#### Initializer <a name="Initializer" id="cdk-constructs.ThronCachePolicyProps.Initializer"></a>

```typescript
import { ThronCachePolicyProps } from 'cdk-constructs'

const thronCachePolicyProps: ThronCachePolicyProps = { ... }
```

#### Properties <a name="Properties" id="Properties"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.ThronCachePolicyProps.property.defaultTtl">defaultTtl</a></code> | <code>aws-cdk-lib.Duration</code> | *No description.* |
| <code><a href="#cdk-constructs.ThronCachePolicyProps.property.maxTtl">maxTtl</a></code> | <code>aws-cdk-lib.Duration</code> | *No description.* |
| <code><a href="#cdk-constructs.ThronCachePolicyProps.property.minTtl">minTtl</a></code> | <code>aws-cdk-lib.Duration</code> | *No description.* |

---

##### `defaultTtl`<sup>Optional</sup> <a name="defaultTtl" id="cdk-constructs.ThronCachePolicyProps.property.defaultTtl"></a>

```typescript
public readonly defaultTtl: Duration;
```

- *Type:* aws-cdk-lib.Duration

---

##### `maxTtl`<sup>Optional</sup> <a name="maxTtl" id="cdk-constructs.ThronCachePolicyProps.property.maxTtl"></a>

```typescript
public readonly maxTtl: Duration;
```

- *Type:* aws-cdk-lib.Duration

---

##### `minTtl`<sup>Optional</sup> <a name="minTtl" id="cdk-constructs.ThronCachePolicyProps.property.minTtl"></a>

```typescript
public readonly minTtl: Duration;
```

- *Type:* aws-cdk-lib.Duration

---

### ThronCloudFrontDistributionProps <a name="ThronCloudFrontDistributionProps" id="cdk-constructs.ThronCloudFrontDistributionProps"></a>

#### Initializer <a name="Initializer" id="cdk-constructs.ThronCloudFrontDistributionProps.Initializer"></a>

```typescript
import { ThronCloudFrontDistributionProps } from 'cdk-constructs'

const thronCloudFrontDistributionProps: ThronCloudFrontDistributionProps = { ... }
```

#### Properties <a name="Properties" id="Properties"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.ThronCloudFrontDistributionProps.property.domainName">domainName</a></code> | <code>string</code> | Validated FQDN. |
| <code><a href="#cdk-constructs.ThronCloudFrontDistributionProps.property.source">source</a></code> | <code>string</code> | Source path from which to deploy the contents of frontend. |
| <code><a href="#cdk-constructs.ThronCloudFrontDistributionProps.property.cachePolicy">cachePolicy</a></code> | <code><a href="#cdk-constructs.ThronCachePolicy">ThronCachePolicy</a></code> | CloudFront's Cache Policy to use on the distribution. |
| <code><a href="#cdk-constructs.ThronCloudFrontDistributionProps.property.defaultRootObject">defaultRootObject</a></code> | <code>string</code> | Object that you want CloudFront to request from your origin when a user requests the root URL for your distribution. |
| <code><a href="#cdk-constructs.ThronCloudFrontDistributionProps.property.defaultRootObjectCachePolicy">defaultRootObjectCachePolicy</a></code> | <code><a href="#cdk-constructs.ThronCachePolicy">ThronCachePolicy</a></code> | *No description.* |
| <code><a href="#cdk-constructs.ThronCloudFrontDistributionProps.property.defaultRootObjectResponseHeaderPolicy">defaultRootObjectResponseHeaderPolicy</a></code> | <code><a href="#cdk-constructs.ThronResponseHeaderPolicy">ThronResponseHeaderPolicy</a></code> | CloudFront's Response Header Policy to use on the distribution. |
| <code><a href="#cdk-constructs.ThronCloudFrontDistributionProps.property.description">description</a></code> | <code>string</code> | Description of the cloudfront distribution; |
| <code><a href="#cdk-constructs.ThronCloudFrontDistributionProps.property.prune">prune</a></code> | <code>boolean</code> | If this is set to false, files in the destination bucket that do not exist in the asset, will NOT be deleted during deployment (create/update). |
| <code><a href="#cdk-constructs.ThronCloudFrontDistributionProps.property.responseHeaderPolicy">responseHeaderPolicy</a></code> | <code><a href="#cdk-constructs.ThronResponseHeaderPolicy">ThronResponseHeaderPolicy</a></code> | CloudFront's Response Header Policy to use on the distribution. |
| <code><a href="#cdk-constructs.ThronCloudFrontDistributionProps.property.version">version</a></code> | <code>string</code> | Prefix key used for versioning the s3 deployment bucket. |

---

##### `domainName`<sup>Required</sup> <a name="domainName" id="cdk-constructs.ThronCloudFrontDistributionProps.property.domainName"></a>

```typescript
public readonly domainName: string;
```

- *Type:* string

Validated FQDN.

---

##### `source`<sup>Required</sup> <a name="source" id="cdk-constructs.ThronCloudFrontDistributionProps.property.source"></a>

```typescript
public readonly source: string;
```

- *Type:* string

Source path from which to deploy the contents of frontend.

---

##### `cachePolicy`<sup>Optional</sup> <a name="cachePolicy" id="cdk-constructs.ThronCloudFrontDistributionProps.property.cachePolicy"></a>

```typescript
public readonly cachePolicy: ThronCachePolicy;
```

- *Type:* <a href="#cdk-constructs.ThronCachePolicy">ThronCachePolicy</a>

CloudFront's Cache Policy to use on the distribution.

---

##### `defaultRootObject`<sup>Optional</sup> <a name="defaultRootObject" id="cdk-constructs.ThronCloudFrontDistributionProps.property.defaultRootObject"></a>

```typescript
public readonly defaultRootObject: string;
```

- *Type:* string

Object that you want CloudFront to request from your origin when a user requests the root URL for your distribution.

---

##### `defaultRootObjectCachePolicy`<sup>Optional</sup> <a name="defaultRootObjectCachePolicy" id="cdk-constructs.ThronCloudFrontDistributionProps.property.defaultRootObjectCachePolicy"></a>

```typescript
public readonly defaultRootObjectCachePolicy: ThronCachePolicy;
```

- *Type:* <a href="#cdk-constructs.ThronCachePolicy">ThronCachePolicy</a>

---

##### `defaultRootObjectResponseHeaderPolicy`<sup>Optional</sup> <a name="defaultRootObjectResponseHeaderPolicy" id="cdk-constructs.ThronCloudFrontDistributionProps.property.defaultRootObjectResponseHeaderPolicy"></a>

```typescript
public readonly defaultRootObjectResponseHeaderPolicy: ThronResponseHeaderPolicy;
```

- *Type:* <a href="#cdk-constructs.ThronResponseHeaderPolicy">ThronResponseHeaderPolicy</a>

CloudFront's Response Header Policy to use on the distribution.

---

##### `description`<sup>Optional</sup> <a name="description" id="cdk-constructs.ThronCloudFrontDistributionProps.property.description"></a>

```typescript
public readonly description: string;
```

- *Type:* string

Description of the cloudfront distribution;

defaults to `domainName`

---

##### `prune`<sup>Optional</sup> <a name="prune" id="cdk-constructs.ThronCloudFrontDistributionProps.property.prune"></a>

```typescript
public readonly prune: boolean;
```

- *Type:* boolean
- *Default:* true

If this is set to false, files in the destination bucket that do not exist in the asset, will NOT be deleted during deployment (create/update).

---

##### `responseHeaderPolicy`<sup>Optional</sup> <a name="responseHeaderPolicy" id="cdk-constructs.ThronCloudFrontDistributionProps.property.responseHeaderPolicy"></a>

```typescript
public readonly responseHeaderPolicy: ThronResponseHeaderPolicy;
```

- *Type:* <a href="#cdk-constructs.ThronResponseHeaderPolicy">ThronResponseHeaderPolicy</a>

CloudFront's Response Header Policy to use on the distribution.

---

##### `version`<sup>Optional</sup> <a name="version" id="cdk-constructs.ThronCloudFrontDistributionProps.property.version"></a>

```typescript
public readonly version: string;
```

- *Type:* string

Prefix key used for versioning the s3 deployment bucket.

---

### ThronCreatedApiGatewayEndpoint <a name="ThronCreatedApiGatewayEndpoint" id="cdk-constructs.ThronCreatedApiGatewayEndpoint"></a>

#### Initializer <a name="Initializer" id="cdk-constructs.ThronCreatedApiGatewayEndpoint.Initializer"></a>

```typescript
import { ThronCreatedApiGatewayEndpoint } from 'cdk-constructs'

const thronCreatedApiGatewayEndpoint: ThronCreatedApiGatewayEndpoint = { ... }
```

#### Properties <a name="Properties" id="Properties"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.ThronCreatedApiGatewayEndpoint.property.apiGatewayApi">apiGatewayApi</a></code> | <code><a href="#cdk-constructs.ThronApiGatewayApi">ThronApiGatewayApi</a></code> | The ThronApiGatewayApi associated with the endpoint. |
| <code><a href="#cdk-constructs.ThronCreatedApiGatewayEndpoint.property.fullEndpoint">fullEndpoint</a></code> | <code>string</code> | The full uri of the exposed api endpoint, i.e `awsd04-product-api-adv1-productimports.4me.cdndev.weebo.it/api/adv1/productimports/`. |
| <code><a href="#cdk-constructs.ThronCreatedApiGatewayEndpoint.property.mainDomain">mainDomain</a></code> | <code>string</code> | The main domain of the api gateway endpoint, i.e `awsd04-product-api-adv1-productimports.4me.cdndev.weebo.it`. |
| <code><a href="#cdk-constructs.ThronCreatedApiGatewayEndpoint.property.path">path</a></code> | <code>string</code> | The path of the exposed api endpoint, i.e `/api/adv1/productimports/`. |

---

##### `apiGatewayApi`<sup>Required</sup> <a name="apiGatewayApi" id="cdk-constructs.ThronCreatedApiGatewayEndpoint.property.apiGatewayApi"></a>

```typescript
public readonly apiGatewayApi: ThronApiGatewayApi;
```

- *Type:* <a href="#cdk-constructs.ThronApiGatewayApi">ThronApiGatewayApi</a>

The ThronApiGatewayApi associated with the endpoint.

---

##### `fullEndpoint`<sup>Required</sup> <a name="fullEndpoint" id="cdk-constructs.ThronCreatedApiGatewayEndpoint.property.fullEndpoint"></a>

```typescript
public readonly fullEndpoint: string;
```

- *Type:* string

The full uri of the exposed api endpoint, i.e `awsd04-product-api-adv1-productimports.4me.cdndev.weebo.it/api/adv1/productimports/`.

---

##### `mainDomain`<sup>Required</sup> <a name="mainDomain" id="cdk-constructs.ThronCreatedApiGatewayEndpoint.property.mainDomain"></a>

```typescript
public readonly mainDomain: string;
```

- *Type:* string

The main domain of the api gateway endpoint, i.e `awsd04-product-api-adv1-productimports.4me.cdndev.weebo.it`.

---

##### `path`<sup>Required</sup> <a name="path" id="cdk-constructs.ThronCreatedApiGatewayEndpoint.property.path"></a>

```typescript
public readonly path: string;
```

- *Type:* string

The path of the exposed api endpoint, i.e `/api/adv1/productimports/`.

---

### ThronEc2ServiceProps <a name="ThronEc2ServiceProps" id="cdk-constructs.ThronEc2ServiceProps"></a>

#### Initializer <a name="Initializer" id="cdk-constructs.ThronEc2ServiceProps.Initializer"></a>

```typescript
import { ThronEc2ServiceProps } from 'cdk-constructs'

const thronEc2ServiceProps: ThronEc2ServiceProps = { ... }
```

#### Properties <a name="Properties" id="Properties"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.ThronEc2ServiceProps.property.cpu">cpu</a></code> | <code>number</code> | The number of cpu units used by the task. |
| <code><a href="#cdk-constructs.ThronEc2ServiceProps.property.ram">ram</a></code> | <code>number</code> | The amount (in MiB) of memory used by the task. |
| <code><a href="#cdk-constructs.ThronEc2ServiceProps.property.containerImage">containerImage</a></code> | <code>aws-cdk-lib.aws_ecs.ContainerImage</code> | Container image to use for the container. |
| <code><a href="#cdk-constructs.ThronEc2ServiceProps.property.environment">environment</a></code> | <code>{[ key: string ]: string}</code> | The environment variables to pass to the container. |
| <code><a href="#cdk-constructs.ThronEc2ServiceProps.property.port">port</a></code> | <code>number</code> | The port exposed for connection. |
| <code><a href="#cdk-constructs.ThronEc2ServiceProps.property.prometheusMetricsPath">prometheusMetricsPath</a></code> | <code>string</code> | Path where Prometheus metrics are exposed. |
| <code><a href="#cdk-constructs.ThronEc2ServiceProps.property.secrets">secrets</a></code> | <code>{[ key: string ]: aws-cdk-lib.aws_ecs.Secret}</code> | The secrets to pass to the container (got by valueFrom). |
| <code><a href="#cdk-constructs.ThronEc2ServiceProps.property.cluster">cluster</a></code> | <code><a href="#cdk-constructs.ClusterOption">ClusterOption</a></code> | *No description.* |
| <code><a href="#cdk-constructs.ThronEc2ServiceProps.property.dockerContextPath">dockerContextPath</a></code> | <code>string</code> | Context of docker build. |
| <code><a href="#cdk-constructs.ThronEc2ServiceProps.property.dockerfileName">dockerfileName</a></code> | <code>string</code> | Name of Dockerfile. |
| <code><a href="#cdk-constructs.ThronEc2ServiceProps.property.endpoints">endpoints</a></code> | <code>{[ key: string ]: <a href="#cdk-constructs.ThronEndpointAlbProps">ThronEndpointAlbProps</a>}</code> | Endpoints associated with this service. |
| <code><a href="#cdk-constructs.ThronEc2ServiceProps.property.healthCheck">healthCheck</a></code> | <code>aws-cdk-lib.aws_elasticloadbalancingv2.HealthCheck</code> | Default healthcheck override. |
| <code><a href="#cdk-constructs.ThronEc2ServiceProps.property.legacyEndpoints">legacyEndpoints</a></code> | <code>{[ key: string ]: <a href="#cdk-constructs.LegacyEndpointAlbProps">LegacyEndpointAlbProps</a>}</code> | Legacy endpoints associated with this service. |
| <code><a href="#cdk-constructs.ThronEc2ServiceProps.property.targetScaling">targetScaling</a></code> | <code><a href="#cdk-constructs.ThronTargetScalingProps">ThronTargetScalingProps</a></code> | *No description.* |

---

##### `cpu`<sup>Required</sup> <a name="cpu" id="cdk-constructs.ThronEc2ServiceProps.property.cpu"></a>

```typescript
public readonly cpu: number;
```

- *Type:* number

The number of cpu units used by the task.

---

##### `ram`<sup>Required</sup> <a name="ram" id="cdk-constructs.ThronEc2ServiceProps.property.ram"></a>

```typescript
public readonly ram: number;
```

- *Type:* number

The amount (in MiB) of memory used by the task.

---

##### `containerImage`<sup>Optional</sup> <a name="containerImage" id="cdk-constructs.ThronEc2ServiceProps.property.containerImage"></a>

```typescript
public readonly containerImage: ContainerImage;
```

- *Type:* aws-cdk-lib.aws_ecs.ContainerImage

Container image to use for the container.

---

##### `environment`<sup>Optional</sup> <a name="environment" id="cdk-constructs.ThronEc2ServiceProps.property.environment"></a>

```typescript
public readonly environment: {[ key: string ]: string};
```

- *Type:* {[ key: string ]: string}
- *Default:* No environment variables.

The environment variables to pass to the container.

---

##### `port`<sup>Optional</sup> <a name="port" id="cdk-constructs.ThronEc2ServiceProps.property.port"></a>

```typescript
public readonly port: number;
```

- *Type:* number

The port exposed for connection.

---

##### `prometheusMetricsPath`<sup>Optional</sup> <a name="prometheusMetricsPath" id="cdk-constructs.ThronEc2ServiceProps.property.prometheusMetricsPath"></a>

```typescript
public readonly prometheusMetricsPath: string;
```

- *Type:* string

Path where Prometheus metrics are exposed.

---

##### `secrets`<sup>Optional</sup> <a name="secrets" id="cdk-constructs.ThronEc2ServiceProps.property.secrets"></a>

```typescript
public readonly secrets: {[ key: string ]: Secret};
```

- *Type:* {[ key: string ]: aws-cdk-lib.aws_ecs.Secret}

The secrets to pass to the container (got by valueFrom).

---

##### `cluster`<sup>Required</sup> <a name="cluster" id="cdk-constructs.ThronEc2ServiceProps.property.cluster"></a>

```typescript
public readonly cluster: ClusterOption;
```

- *Type:* <a href="#cdk-constructs.ClusterOption">ClusterOption</a>

---

##### `dockerContextPath`<sup>Required</sup> <a name="dockerContextPath" id="cdk-constructs.ThronEc2ServiceProps.property.dockerContextPath"></a>

```typescript
public readonly dockerContextPath: string;
```

- *Type:* string

Context of docker build.

---

##### `dockerfileName`<sup>Optional</sup> <a name="dockerfileName" id="cdk-constructs.ThronEc2ServiceProps.property.dockerfileName"></a>

```typescript
public readonly dockerfileName: string;
```

- *Type:* string
- *Default:* Dockerfile

Name of Dockerfile.

---

##### `endpoints`<sup>Optional</sup> <a name="endpoints" id="cdk-constructs.ThronEc2ServiceProps.property.endpoints"></a>

```typescript
public readonly endpoints: {[ key: string ]: ThronEndpointAlbProps};
```

- *Type:* {[ key: string ]: <a href="#cdk-constructs.ThronEndpointAlbProps">ThronEndpointAlbProps</a>}

Endpoints associated with this service.

---

##### `healthCheck`<sup>Optional</sup> <a name="healthCheck" id="cdk-constructs.ThronEc2ServiceProps.property.healthCheck"></a>

```typescript
public readonly healthCheck: HealthCheck;
```

- *Type:* aws-cdk-lib.aws_elasticloadbalancingv2.HealthCheck

Default healthcheck override.

---

##### `legacyEndpoints`<sup>Optional</sup> <a name="legacyEndpoints" id="cdk-constructs.ThronEc2ServiceProps.property.legacyEndpoints"></a>

```typescript
public readonly legacyEndpoints: {[ key: string ]: LegacyEndpointAlbProps};
```

- *Type:* {[ key: string ]: <a href="#cdk-constructs.LegacyEndpointAlbProps">LegacyEndpointAlbProps</a>}

Legacy endpoints associated with this service.

---

##### `targetScaling`<sup>Optional</sup> <a name="targetScaling" id="cdk-constructs.ThronEc2ServiceProps.property.targetScaling"></a>

```typescript
public readonly targetScaling: ThronTargetScalingProps;
```

- *Type:* <a href="#cdk-constructs.ThronTargetScalingProps">ThronTargetScalingProps</a>

---

### ThronEc2TargetScalingProps <a name="ThronEc2TargetScalingProps" id="cdk-constructs.ThronEc2TargetScalingProps"></a>

#### Initializer <a name="Initializer" id="cdk-constructs.ThronEc2TargetScalingProps.Initializer"></a>

```typescript
import { ThronEc2TargetScalingProps } from 'cdk-constructs'

const thronEc2TargetScalingProps: ThronEc2TargetScalingProps = { ... }
```

#### Properties <a name="Properties" id="Properties"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.ThronEc2TargetScalingProps.property.maxCapacity">maxCapacity</a></code> | <code>number</code> | The maximum value that Application Auto Scaling can use to scale a target during a scaling activity. |
| <code><a href="#cdk-constructs.ThronEc2TargetScalingProps.property.minCapacity">minCapacity</a></code> | <code>number</code> | The minimum value that Application Auto Scaling can use to scale a target during a scaling activity. |
| <code><a href="#cdk-constructs.ThronEc2TargetScalingProps.property.targetValue">targetValue</a></code> | <code>number</code> | The target value for the metric. |
| <code><a href="#cdk-constructs.ThronEc2TargetScalingProps.property.predefinedMetric">predefinedMetric</a></code> | <code>aws-cdk-lib.aws_applicationautoscaling.PredefinedMetric</code> | A predefined metric for application autoscaling. |
| <code><a href="#cdk-constructs.ThronEc2TargetScalingProps.property.scaleInCooldown">scaleInCooldown</a></code> | <code>aws-cdk-lib.Duration</code> | The amount of time after a scale in activity completes before another scale in activity can start. |
| <code><a href="#cdk-constructs.ThronEc2TargetScalingProps.property.scaleOutCooldown">scaleOutCooldown</a></code> | <code>aws-cdk-lib.Duration</code> | The amount of time after a scale in activity completes before another scale in activity can start. |
| <code><a href="#cdk-constructs.ThronEc2TargetScalingProps.property.ec2Service">ec2Service</a></code> | <code>aws-cdk-lib.aws_ecs.Ec2Service</code> | Ec2 Service used as target resource. |

---

##### `maxCapacity`<sup>Required</sup> <a name="maxCapacity" id="cdk-constructs.ThronEc2TargetScalingProps.property.maxCapacity"></a>

```typescript
public readonly maxCapacity: number;
```

- *Type:* number

The maximum value that Application Auto Scaling can use to scale a target during a scaling activity.

---

##### `minCapacity`<sup>Required</sup> <a name="minCapacity" id="cdk-constructs.ThronEc2TargetScalingProps.property.minCapacity"></a>

```typescript
public readonly minCapacity: number;
```

- *Type:* number

The minimum value that Application Auto Scaling can use to scale a target during a scaling activity.

---

##### `targetValue`<sup>Required</sup> <a name="targetValue" id="cdk-constructs.ThronEc2TargetScalingProps.property.targetValue"></a>

```typescript
public readonly targetValue: number;
```

- *Type:* number

The target value for the metric.

---

##### `predefinedMetric`<sup>Optional</sup> <a name="predefinedMetric" id="cdk-constructs.ThronEc2TargetScalingProps.property.predefinedMetric"></a>

```typescript
public readonly predefinedMetric: PredefinedMetric;
```

- *Type:* aws-cdk-lib.aws_applicationautoscaling.PredefinedMetric

A predefined metric for application autoscaling.

The metric must track utilization. Scaling out will happen if the metric is higher than the target value,
scaling in will happen in the metric is lower than the target value.

---

##### `scaleInCooldown`<sup>Optional</sup> <a name="scaleInCooldown" id="cdk-constructs.ThronEc2TargetScalingProps.property.scaleInCooldown"></a>

```typescript
public readonly scaleInCooldown: Duration;
```

- *Type:* aws-cdk-lib.Duration
- *Default:* Duration.minutes(300)

The amount of time after a scale in activity completes before another scale in activity can start.

---

##### `scaleOutCooldown`<sup>Optional</sup> <a name="scaleOutCooldown" id="cdk-constructs.ThronEc2TargetScalingProps.property.scaleOutCooldown"></a>

```typescript
public readonly scaleOutCooldown: Duration;
```

- *Type:* aws-cdk-lib.Duration
- *Default:* Duration.minutes(90)

The amount of time after a scale in activity completes before another scale in activity can start.

---

##### `ec2Service`<sup>Required</sup> <a name="ec2Service" id="cdk-constructs.ThronEc2TargetScalingProps.property.ec2Service"></a>

```typescript
public readonly ec2Service: Ec2Service;
```

- *Type:* aws-cdk-lib.aws_ecs.Ec2Service

Ec2 Service used as target resource.

---

### ThronEc2TaskDefinitionProps <a name="ThronEc2TaskDefinitionProps" id="cdk-constructs.ThronEc2TaskDefinitionProps"></a>

#### Initializer <a name="Initializer" id="cdk-constructs.ThronEc2TaskDefinitionProps.Initializer"></a>

```typescript
import { ThronEc2TaskDefinitionProps } from 'cdk-constructs'

const thronEc2TaskDefinitionProps: ThronEc2TaskDefinitionProps = { ... }
```

#### Properties <a name="Properties" id="Properties"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.ThronEc2TaskDefinitionProps.property.cpu">cpu</a></code> | <code>number</code> | The number of cpu units used by the task. |
| <code><a href="#cdk-constructs.ThronEc2TaskDefinitionProps.property.ram">ram</a></code> | <code>number</code> | The amount (in MiB) of memory used by the task. |
| <code><a href="#cdk-constructs.ThronEc2TaskDefinitionProps.property.containerImage">containerImage</a></code> | <code>aws-cdk-lib.aws_ecs.ContainerImage</code> | Container image to use for the container. |
| <code><a href="#cdk-constructs.ThronEc2TaskDefinitionProps.property.environment">environment</a></code> | <code>{[ key: string ]: string}</code> | The environment variables to pass to the container. |
| <code><a href="#cdk-constructs.ThronEc2TaskDefinitionProps.property.port">port</a></code> | <code>number</code> | The port exposed for connection. |
| <code><a href="#cdk-constructs.ThronEc2TaskDefinitionProps.property.prometheusMetricsPath">prometheusMetricsPath</a></code> | <code>string</code> | Path where Prometheus metrics are exposed. |
| <code><a href="#cdk-constructs.ThronEc2TaskDefinitionProps.property.secrets">secrets</a></code> | <code>{[ key: string ]: aws-cdk-lib.aws_ecs.Secret}</code> | The secrets to pass to the container (got by valueFrom). |

---

##### `cpu`<sup>Required</sup> <a name="cpu" id="cdk-constructs.ThronEc2TaskDefinitionProps.property.cpu"></a>

```typescript
public readonly cpu: number;
```

- *Type:* number

The number of cpu units used by the task.

---

##### `ram`<sup>Required</sup> <a name="ram" id="cdk-constructs.ThronEc2TaskDefinitionProps.property.ram"></a>

```typescript
public readonly ram: number;
```

- *Type:* number

The amount (in MiB) of memory used by the task.

---

##### `containerImage`<sup>Optional</sup> <a name="containerImage" id="cdk-constructs.ThronEc2TaskDefinitionProps.property.containerImage"></a>

```typescript
public readonly containerImage: ContainerImage;
```

- *Type:* aws-cdk-lib.aws_ecs.ContainerImage

Container image to use for the container.

---

##### `environment`<sup>Optional</sup> <a name="environment" id="cdk-constructs.ThronEc2TaskDefinitionProps.property.environment"></a>

```typescript
public readonly environment: {[ key: string ]: string};
```

- *Type:* {[ key: string ]: string}
- *Default:* No environment variables.

The environment variables to pass to the container.

---

##### `port`<sup>Optional</sup> <a name="port" id="cdk-constructs.ThronEc2TaskDefinitionProps.property.port"></a>

```typescript
public readonly port: number;
```

- *Type:* number

The port exposed for connection.

---

##### `prometheusMetricsPath`<sup>Optional</sup> <a name="prometheusMetricsPath" id="cdk-constructs.ThronEc2TaskDefinitionProps.property.prometheusMetricsPath"></a>

```typescript
public readonly prometheusMetricsPath: string;
```

- *Type:* string

Path where Prometheus metrics are exposed.

---

##### `secrets`<sup>Optional</sup> <a name="secrets" id="cdk-constructs.ThronEc2TaskDefinitionProps.property.secrets"></a>

```typescript
public readonly secrets: {[ key: string ]: Secret};
```

- *Type:* {[ key: string ]: aws-cdk-lib.aws_ecs.Secret}

The secrets to pass to the container (got by valueFrom).

---

### ThronEndpointAlbProps <a name="ThronEndpointAlbProps" id="cdk-constructs.ThronEndpointAlbProps"></a>

#### Initializer <a name="Initializer" id="cdk-constructs.ThronEndpointAlbProps.Initializer"></a>

```typescript
import { ThronEndpointAlbProps } from 'cdk-constructs'

const thronEndpointAlbProps: ThronEndpointAlbProps = { ... }
```

#### Properties <a name="Properties" id="Properties"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.ThronEndpointAlbProps.property.serviceGroup">serviceGroup</a></code> | <code><a href="#cdk-constructs.ServiceGroup">ServiceGroup</a></code> | Service group of the service. |
| <code><a href="#cdk-constructs.ThronEndpointAlbProps.property.serviceName">serviceName</a></code> | <code>string</code> | Name of the service the endpoint exposes. |
| <code><a href="#cdk-constructs.ThronEndpointAlbProps.property.stack">stack</a></code> | <code>aws-cdk-lib.Stack</code> | The reference of parent Stack. |
| <code><a href="#cdk-constructs.ThronEndpointAlbProps.property.version">version</a></code> | <code>number</code> | The version of the API exposed by the endpoint. |
| <code><a href="#cdk-constructs.ThronEndpointAlbProps.property.visibility">visibility</a></code> | <code><a href="#cdk-constructs.EndpointVisibility">EndpointVisibility</a></code> | Wether the endpoint is private or public. |

---

##### `serviceGroup`<sup>Required</sup> <a name="serviceGroup" id="cdk-constructs.ThronEndpointAlbProps.property.serviceGroup"></a>

```typescript
public readonly serviceGroup: ServiceGroup;
```

- *Type:* <a href="#cdk-constructs.ServiceGroup">ServiceGroup</a>

Service group of the service.

---

##### `serviceName`<sup>Required</sup> <a name="serviceName" id="cdk-constructs.ThronEndpointAlbProps.property.serviceName"></a>

```typescript
public readonly serviceName: string;
```

- *Type:* string

Name of the service the endpoint exposes.

---

##### `stack`<sup>Optional</sup> <a name="stack" id="cdk-constructs.ThronEndpointAlbProps.property.stack"></a>

```typescript
public readonly stack: Stack;
```

- *Type:* aws-cdk-lib.Stack

The reference of parent Stack.

---

##### `version`<sup>Optional</sup> <a name="version" id="cdk-constructs.ThronEndpointAlbProps.property.version"></a>

```typescript
public readonly version: number;
```

- *Type:* number
- *Default:* 1

The version of the API exposed by the endpoint.

---

##### `visibility`<sup>Optional</sup> <a name="visibility" id="cdk-constructs.ThronEndpointAlbProps.property.visibility"></a>

```typescript
public readonly visibility: EndpointVisibility;
```

- *Type:* <a href="#cdk-constructs.EndpointVisibility">EndpointVisibility</a>
- *Default:* EndpointVisibility.PRIVATE

Wether the endpoint is private or public.

---

### ThronEndpointApiGatewayProps <a name="ThronEndpointApiGatewayProps" id="cdk-constructs.ThronEndpointApiGatewayProps"></a>

#### Initializer <a name="Initializer" id="cdk-constructs.ThronEndpointApiGatewayProps.Initializer"></a>

```typescript
import { ThronEndpointApiGatewayProps } from 'cdk-constructs'

const thronEndpointApiGatewayProps: ThronEndpointApiGatewayProps = { ... }
```

#### Properties <a name="Properties" id="Properties"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.ThronEndpointApiGatewayProps.property.apiGatewayApi">apiGatewayApi</a></code> | <code>aws-cdk-lib.aws_apigateway.IRestApi</code> | The API on which the endpoint should be added. |
| <code><a href="#cdk-constructs.ThronEndpointApiGatewayProps.property.basePath">basePath</a></code> | <code>string</code> | The path on which to add the endpoint. |
| <code><a href="#cdk-constructs.ThronEndpointApiGatewayProps.property.lambdaFunction">lambdaFunction</a></code> | <code>aws-cdk-lib.aws_lambda.IFunction</code> | The function to attach to the endpoint. |
| <code><a href="#cdk-constructs.ThronEndpointApiGatewayProps.property.timeout">timeout</a></code> | <code>aws-cdk-lib.Duration</code> | The timeout of the integration. |

---

##### `apiGatewayApi`<sup>Required</sup> <a name="apiGatewayApi" id="cdk-constructs.ThronEndpointApiGatewayProps.property.apiGatewayApi"></a>

```typescript
public readonly apiGatewayApi: IRestApi;
```

- *Type:* aws-cdk-lib.aws_apigateway.IRestApi

The API on which the endpoint should be added.

---

##### `basePath`<sup>Required</sup> <a name="basePath" id="cdk-constructs.ThronEndpointApiGatewayProps.property.basePath"></a>

```typescript
public readonly basePath: string;
```

- *Type:* string

The path on which to add the endpoint.

---

##### `lambdaFunction`<sup>Required</sup> <a name="lambdaFunction" id="cdk-constructs.ThronEndpointApiGatewayProps.property.lambdaFunction"></a>

```typescript
public readonly lambdaFunction: IFunction;
```

- *Type:* aws-cdk-lib.aws_lambda.IFunction

The function to attach to the endpoint.

---

##### `timeout`<sup>Required</sup> <a name="timeout" id="cdk-constructs.ThronEndpointApiGatewayProps.property.timeout"></a>

```typescript
public readonly timeout: Duration;
```

- *Type:* aws-cdk-lib.Duration

The timeout of the integration.

---

### ThronHealthCheckOverride <a name="ThronHealthCheckOverride" id="cdk-constructs.ThronHealthCheckOverride"></a>

#### Initializer <a name="Initializer" id="cdk-constructs.ThronHealthCheckOverride.Initializer"></a>

```typescript
import { ThronHealthCheckOverride } from 'cdk-constructs'

const thronHealthCheckOverride: ThronHealthCheckOverride = { ... }
```

#### Properties <a name="Properties" id="Properties"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.ThronHealthCheckOverride.property.healthyHttpCodes">healthyHttpCodes</a></code> | <code>string</code> | *No description.* |
| <code><a href="#cdk-constructs.ThronHealthCheckOverride.property.healthyThresholdCount">healthyThresholdCount</a></code> | <code>number</code> | *No description.* |
| <code><a href="#cdk-constructs.ThronHealthCheckOverride.property.interval">interval</a></code> | <code>aws-cdk-lib.Duration</code> | *No description.* |
| <code><a href="#cdk-constructs.ThronHealthCheckOverride.property.path">path</a></code> | <code>string</code> | *No description.* |
| <code><a href="#cdk-constructs.ThronHealthCheckOverride.property.port">port</a></code> | <code>string</code> | *No description.* |
| <code><a href="#cdk-constructs.ThronHealthCheckOverride.property.timeout">timeout</a></code> | <code>aws-cdk-lib.Duration</code> | *No description.* |
| <code><a href="#cdk-constructs.ThronHealthCheckOverride.property.unhealthyThresholdCount">unhealthyThresholdCount</a></code> | <code>number</code> | *No description.* |

---

##### `healthyHttpCodes`<sup>Optional</sup> <a name="healthyHttpCodes" id="cdk-constructs.ThronHealthCheckOverride.property.healthyHttpCodes"></a>

```typescript
public readonly healthyHttpCodes: string;
```

- *Type:* string

---

##### `healthyThresholdCount`<sup>Optional</sup> <a name="healthyThresholdCount" id="cdk-constructs.ThronHealthCheckOverride.property.healthyThresholdCount"></a>

```typescript
public readonly healthyThresholdCount: number;
```

- *Type:* number

---

##### `interval`<sup>Optional</sup> <a name="interval" id="cdk-constructs.ThronHealthCheckOverride.property.interval"></a>

```typescript
public readonly interval: Duration;
```

- *Type:* aws-cdk-lib.Duration

---

##### `path`<sup>Optional</sup> <a name="path" id="cdk-constructs.ThronHealthCheckOverride.property.path"></a>

```typescript
public readonly path: string;
```

- *Type:* string

---

##### `port`<sup>Optional</sup> <a name="port" id="cdk-constructs.ThronHealthCheckOverride.property.port"></a>

```typescript
public readonly port: string;
```

- *Type:* string

---

##### `timeout`<sup>Optional</sup> <a name="timeout" id="cdk-constructs.ThronHealthCheckOverride.property.timeout"></a>

```typescript
public readonly timeout: Duration;
```

- *Type:* aws-cdk-lib.Duration

---

##### `unhealthyThresholdCount`<sup>Optional</sup> <a name="unhealthyThresholdCount" id="cdk-constructs.ThronHealthCheckOverride.property.unhealthyThresholdCount"></a>

```typescript
public readonly unhealthyThresholdCount: number;
```

- *Type:* number

---

### ThronLambdaApiGatewayEndpointProps <a name="ThronLambdaApiGatewayEndpointProps" id="cdk-constructs.ThronLambdaApiGatewayEndpointProps"></a>

#### Initializer <a name="Initializer" id="cdk-constructs.ThronLambdaApiGatewayEndpointProps.Initializer"></a>

```typescript
import { ThronLambdaApiGatewayEndpointProps } from 'cdk-constructs'

const thronLambdaApiGatewayEndpointProps: ThronLambdaApiGatewayEndpointProps = { ... }
```

#### Properties <a name="Properties" id="Properties"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.ThronLambdaApiGatewayEndpointProps.property.serviceGroup">serviceGroup</a></code> | <code><a href="#cdk-constructs.ServiceGroup">ServiceGroup</a></code> | Service group of the service. |
| <code><a href="#cdk-constructs.ThronLambdaApiGatewayEndpointProps.property.version">version</a></code> | <code>number</code> | The version of the API exposed by the endpoint. |
| <code><a href="#cdk-constructs.ThronLambdaApiGatewayEndpointProps.property.visibility">visibility</a></code> | <code><a href="#cdk-constructs.EndpointVisibility">EndpointVisibility</a></code> | Wether the endpoint is private or public. |
| <code><a href="#cdk-constructs.ThronLambdaApiGatewayEndpointProps.property.serviceName">serviceName</a></code> | <code>string</code> | Name of the service the endpoint exposes. |
| <code><a href="#cdk-constructs.ThronLambdaApiGatewayEndpointProps.property.apiGatewayOverride">apiGatewayOverride</a></code> | <code><a href="#cdk-constructs.ThronApiGatewayApi">ThronApiGatewayApi</a></code> | If this params is provided, no new Api Gateway will be created. |
| <code><a href="#cdk-constructs.ThronLambdaApiGatewayEndpointProps.property.pathOverride">pathOverride</a></code> | <code>string</code> | If this params is provided, the path of the service will be overridden with the given one. |

---

##### `serviceGroup`<sup>Optional</sup> <a name="serviceGroup" id="cdk-constructs.ThronLambdaApiGatewayEndpointProps.property.serviceGroup"></a>

```typescript
public readonly serviceGroup: ServiceGroup;
```

- *Type:* <a href="#cdk-constructs.ServiceGroup">ServiceGroup</a>
- *Default:* ServiceGroup.VIEW

Service group of the service.

---

##### `version`<sup>Optional</sup> <a name="version" id="cdk-constructs.ThronLambdaApiGatewayEndpointProps.property.version"></a>

```typescript
public readonly version: number;
```

- *Type:* number
- *Default:* 1

The version of the API exposed by the endpoint.

---

##### `visibility`<sup>Optional</sup> <a name="visibility" id="cdk-constructs.ThronLambdaApiGatewayEndpointProps.property.visibility"></a>

```typescript
public readonly visibility: EndpointVisibility;
```

- *Type:* <a href="#cdk-constructs.EndpointVisibility">EndpointVisibility</a>
- *Default:* EndpointVisibility.PRIVATE

Wether the endpoint is private or public.

---

##### `serviceName`<sup>Required</sup> <a name="serviceName" id="cdk-constructs.ThronLambdaApiGatewayEndpointProps.property.serviceName"></a>

```typescript
public readonly serviceName: string;
```

- *Type:* string

Name of the service the endpoint exposes.

---

##### `apiGatewayOverride`<sup>Optional</sup> <a name="apiGatewayOverride" id="cdk-constructs.ThronLambdaApiGatewayEndpointProps.property.apiGatewayOverride"></a>

```typescript
public readonly apiGatewayOverride: ThronApiGatewayApi;
```

- *Type:* <a href="#cdk-constructs.ThronApiGatewayApi">ThronApiGatewayApi</a>

If this params is provided, no new Api Gateway will be created.

Instead, the provided api gateway will be used

---

##### `pathOverride`<sup>Optional</sup> <a name="pathOverride" id="cdk-constructs.ThronLambdaApiGatewayEndpointProps.property.pathOverride"></a>

```typescript
public readonly pathOverride: string;
```

- *Type:* string

If this params is provided, the path of the service will be overridden with the given one.

---

### ThronLambdaMicroservicePipelineProps <a name="ThronLambdaMicroservicePipelineProps" id="cdk-constructs.ThronLambdaMicroservicePipelineProps"></a>

ThronLambdaMicroservicePipeline Props.

#### Initializer <a name="Initializer" id="cdk-constructs.ThronLambdaMicroservicePipelineProps.Initializer"></a>

```typescript
import { ThronLambdaMicroservicePipelineProps } from 'cdk-constructs'

const thronLambdaMicroservicePipelineProps: ThronLambdaMicroservicePipelineProps = { ... }
```

#### Properties <a name="Properties" id="Properties"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.ThronLambdaMicroservicePipelineProps.property.cicdConfig">cicdConfig</a></code> | <code>{[ key: string ]: <a href="#cdk-constructs.CicdEnvironment">CicdEnvironment</a>}</code> | Target accounts for pipeline and other CICD settings. |
| <code><a href="#cdk-constructs.ThronLambdaMicroservicePipelineProps.property.customBuildImage">customBuildImage</a></code> | <code>aws-cdk-lib.aws_codebuild.IBuildImage</code> | Build Image to be used by default in all the lambda steps. |
| <code><a href="#cdk-constructs.ThronLambdaMicroservicePipelineProps.property.lambdas">lambdas</a></code> | <code>{[ key: string ]: <a href="#cdk-constructs.StepConfig">StepConfig</a>}</code> | Map of all the lambdas id along with their {@link StepConfiguration}. |
| <code><a href="#cdk-constructs.ThronLambdaMicroservicePipelineProps.property.projectId">projectId</a></code> | <code>string</code> | Id of the applicative project to use. |
| <code><a href="#cdk-constructs.ThronLambdaMicroservicePipelineProps.property.tests">tests</a></code> | <code>{[ key: string ]: <a href="#cdk-constructs.StepConfig">StepConfig</a>}</code> | Map of all the tests id along with their {@link StepConfiguration}. |
| <code><a href="#cdk-constructs.ThronLambdaMicroservicePipelineProps.property.preExistingArtifactBucket">preExistingArtifactBucket</a></code> | <code>string</code> | If specified, uses an existing bucket for storing artifacts. |
| <code><a href="#cdk-constructs.ThronLambdaMicroservicePipelineProps.property.preExistingRepositoryName">preExistingRepositoryName</a></code> | <code>string</code> | If specified, define a source codecommit repository instead of creating one. |
| <code><a href="#cdk-constructs.ThronLambdaMicroservicePipelineProps.property.projectPreset">projectPreset</a></code> | <code><a href="#cdk-constructs.ProjectPreset">ProjectPreset</a></code> | If specified, the new project will be initialized with the chosen codebase, after the subs have been performed Note: You cannot specify this attribute if `preExistingRepositoryName` is specified. |

---

##### `cicdConfig`<sup>Required</sup> <a name="cicdConfig" id="cdk-constructs.ThronLambdaMicroservicePipelineProps.property.cicdConfig"></a>

```typescript
public readonly cicdConfig: {[ key: string ]: CicdEnvironment};
```

- *Type:* {[ key: string ]: <a href="#cdk-constructs.CicdEnvironment">CicdEnvironment</a>}

Target accounts for pipeline and other CICD settings.

---

##### `customBuildImage`<sup>Required</sup> <a name="customBuildImage" id="cdk-constructs.ThronLambdaMicroservicePipelineProps.property.customBuildImage"></a>

```typescript
public readonly customBuildImage: IBuildImage;
```

- *Type:* aws-cdk-lib.aws_codebuild.IBuildImage

Build Image to be used by default in all the lambda steps.

---

##### `lambdas`<sup>Required</sup> <a name="lambdas" id="cdk-constructs.ThronLambdaMicroservicePipelineProps.property.lambdas"></a>

```typescript
public readonly lambdas: {[ key: string ]: StepConfig};
```

- *Type:* {[ key: string ]: <a href="#cdk-constructs.StepConfig">StepConfig</a>}

Map of all the lambdas id along with their {@link StepConfiguration}.

Lambdas ids must:
- Be between 3 and 25 longs and only letters
- Not be repeated (case insensitive).

---

##### `projectId`<sup>Required</sup> <a name="projectId" id="cdk-constructs.ThronLambdaMicroservicePipelineProps.property.projectId"></a>

```typescript
public readonly projectId: string;
```

- *Type:* string

Id of the applicative project to use.

If the app project is `products-sync`, projectId should be `product-sync`. Resources prefixes will automatically append `-cicd-{env}`
after the prefix. In the aforementioned example, all the resources will be prefixed with `product-sync-cicd-development`, `product-sync-cicd-quality` or `product-sync-cicd-production`
based on the environment

---

##### `tests`<sup>Required</sup> <a name="tests" id="cdk-constructs.ThronLambdaMicroservicePipelineProps.property.tests"></a>

```typescript
public readonly tests: {[ key: string ]: StepConfig};
```

- *Type:* {[ key: string ]: <a href="#cdk-constructs.StepConfig">StepConfig</a>}

Map of all the tests id along with their {@link StepConfiguration}.

Test ids must:
- Be between 3 and 25 longs and only letters
- Not be repeated (case insensitive).

---

##### `preExistingArtifactBucket`<sup>Optional</sup> <a name="preExistingArtifactBucket" id="cdk-constructs.ThronLambdaMicroservicePipelineProps.property.preExistingArtifactBucket"></a>

```typescript
public readonly preExistingArtifactBucket: string;
```

- *Type:* string

If specified, uses an existing bucket for storing artifacts.

---

##### `preExistingRepositoryName`<sup>Optional</sup> <a name="preExistingRepositoryName" id="cdk-constructs.ThronLambdaMicroservicePipelineProps.property.preExistingRepositoryName"></a>

```typescript
public readonly preExistingRepositoryName: string;
```

- *Type:* string

If specified, define a source codecommit repository instead of creating one.

Note: You cannot specify this attribute if `projectPreset` is specified

---

##### `projectPreset`<sup>Optional</sup> <a name="projectPreset" id="cdk-constructs.ThronLambdaMicroservicePipelineProps.property.projectPreset"></a>

```typescript
public readonly projectPreset: ProjectPreset;
```

- *Type:* <a href="#cdk-constructs.ProjectPreset">ProjectPreset</a>

If specified, the new project will be initialized with the chosen codebase, after the subs have been performed Note: You cannot specify this attribute if `preExistingRepositoryName` is specified.

---

*Example*

```typescript
   {
     repositoryBranchTagOrSha: "master",
     repositoryName: "golang-project-template",
     repositoryRegion: "eu-west-1",
     subConfigs: [
       { searchValue: "##project-name##", replaceValue: 'sample-project-id }
     ]
   }
```


### ThronLambdaSingleEnvPipelineCodeCommitProps <a name="ThronLambdaSingleEnvPipelineCodeCommitProps" id="cdk-constructs.ThronLambdaSingleEnvPipelineCodeCommitProps"></a>

Codecommit configuration for the Source Phase of the pipeline.

#### Initializer <a name="Initializer" id="cdk-constructs.ThronLambdaSingleEnvPipelineCodeCommitProps.Initializer"></a>

```typescript
import { ThronLambdaSingleEnvPipelineCodeCommitProps } from 'cdk-constructs'

const thronLambdaSingleEnvPipelineCodeCommitProps: ThronLambdaSingleEnvPipelineCodeCommitProps = { ... }
```

#### Properties <a name="Properties" id="Properties"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.ThronLambdaSingleEnvPipelineCodeCommitProps.property.branch">branch</a></code> | <code>string</code> | Repository branch on which the pipeline trigger is set. |
| <code><a href="#cdk-constructs.ThronLambdaSingleEnvPipelineCodeCommitProps.property.repository">repository</a></code> | <code>aws-cdk-lib.aws_codecommit.IRepository</code> | Repository on which the pipeline trigger is set. |

---

##### `branch`<sup>Required</sup> <a name="branch" id="cdk-constructs.ThronLambdaSingleEnvPipelineCodeCommitProps.property.branch"></a>

```typescript
public readonly branch: string;
```

- *Type:* string

Repository branch on which the pipeline trigger is set.

---

##### `repository`<sup>Required</sup> <a name="repository" id="cdk-constructs.ThronLambdaSingleEnvPipelineCodeCommitProps.property.repository"></a>

```typescript
public readonly repository: IRepository;
```

- *Type:* aws-cdk-lib.aws_codecommit.IRepository

Repository on which the pipeline trigger is set.

---

### ThronLambdaSingleEnvPipelineProps <a name="ThronLambdaSingleEnvPipelineProps" id="cdk-constructs.ThronLambdaSingleEnvPipelineProps"></a>

ThronLambdaSingleEnvPipeline Props.

#### Initializer <a name="Initializer" id="cdk-constructs.ThronLambdaSingleEnvPipelineProps.Initializer"></a>

```typescript
import { ThronLambdaSingleEnvPipelineProps } from 'cdk-constructs'

const thronLambdaSingleEnvPipelineProps: ThronLambdaSingleEnvPipelineProps = { ... }
```

#### Properties <a name="Properties" id="Properties"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.ThronLambdaSingleEnvPipelineProps.property.artifactBucket">artifactBucket</a></code> | <code>aws-cdk-lib.aws_s3.IBucket</code> | The bucket to store the artifacts. |
| <code><a href="#cdk-constructs.ThronLambdaSingleEnvPipelineProps.property.codeCommitConfig">codeCommitConfig</a></code> | <code><a href="#cdk-constructs.ThronLambdaSingleEnvPipelineCodeCommitProps">ThronLambdaSingleEnvPipelineCodeCommitProps</a></code> | The configuration for the code commit repository. |
| <code><a href="#cdk-constructs.ThronLambdaSingleEnvPipelineProps.property.deployConf">deployConf</a></code> | <code><a href="#cdk-constructs.DeployStepConf">DeployStepConf</a></code> | The Configuration for the Deploy Step. |
| <code><a href="#cdk-constructs.ThronLambdaSingleEnvPipelineProps.property.lambdasConf">lambdasConf</a></code> | <code>{[ key: string ]: <a href="#cdk-constructs.LambdaConf">LambdaConf</a>}</code> | Lambda Configurations. |
| <code><a href="#cdk-constructs.ThronLambdaSingleEnvPipelineProps.property.prefix">prefix</a></code> | <code>string</code> | Prefix for resources. |
| <code><a href="#cdk-constructs.ThronLambdaSingleEnvPipelineProps.property.testConf">testConf</a></code> | <code>{[ key: string ]: <a href="#cdk-constructs.StepConfig">StepConfig</a>}</code> | The ids of the tests to run. |
| <code><a href="#cdk-constructs.ThronLambdaSingleEnvPipelineProps.property.isBuildEnabled">isBuildEnabled</a></code> | <code>boolean</code> | Whether or not the build stage is enabled. |
| <code><a href="#cdk-constructs.ThronLambdaSingleEnvPipelineProps.property.notifyConf">notifyConf</a></code> | <code><a href="#cdk-constructs.NotifyConf">NotifyConf</a></code> | Configuration for enabling pipeline notifications. |

---

##### `artifactBucket`<sup>Required</sup> <a name="artifactBucket" id="cdk-constructs.ThronLambdaSingleEnvPipelineProps.property.artifactBucket"></a>

```typescript
public readonly artifactBucket: IBucket;
```

- *Type:* aws-cdk-lib.aws_s3.IBucket

The bucket to store the artifacts.

---

##### `codeCommitConfig`<sup>Required</sup> <a name="codeCommitConfig" id="cdk-constructs.ThronLambdaSingleEnvPipelineProps.property.codeCommitConfig"></a>

```typescript
public readonly codeCommitConfig: ThronLambdaSingleEnvPipelineCodeCommitProps;
```

- *Type:* <a href="#cdk-constructs.ThronLambdaSingleEnvPipelineCodeCommitProps">ThronLambdaSingleEnvPipelineCodeCommitProps</a>

The configuration for the code commit repository.

---

##### `deployConf`<sup>Required</sup> <a name="deployConf" id="cdk-constructs.ThronLambdaSingleEnvPipelineProps.property.deployConf"></a>

```typescript
public readonly deployConf: DeployStepConf;
```

- *Type:* <a href="#cdk-constructs.DeployStepConf">DeployStepConf</a>

The Configuration for the Deploy Step.

---

##### `lambdasConf`<sup>Required</sup> <a name="lambdasConf" id="cdk-constructs.ThronLambdaSingleEnvPipelineProps.property.lambdasConf"></a>

```typescript
public readonly lambdasConf: {[ key: string ]: LambdaConf};
```

- *Type:* {[ key: string ]: <a href="#cdk-constructs.LambdaConf">LambdaConf</a>}

Lambda Configurations.

---

##### `prefix`<sup>Required</sup> <a name="prefix" id="cdk-constructs.ThronLambdaSingleEnvPipelineProps.property.prefix"></a>

```typescript
public readonly prefix: string;
```

- *Type:* string

Prefix for resources.

---

##### `testConf`<sup>Required</sup> <a name="testConf" id="cdk-constructs.ThronLambdaSingleEnvPipelineProps.property.testConf"></a>

```typescript
public readonly testConf: {[ key: string ]: StepConfig};
```

- *Type:* {[ key: string ]: <a href="#cdk-constructs.StepConfig">StepConfig</a>}

The ids of the tests to run.

---

##### `isBuildEnabled`<sup>Optional</sup> <a name="isBuildEnabled" id="cdk-constructs.ThronLambdaSingleEnvPipelineProps.property.isBuildEnabled"></a>

```typescript
public readonly isBuildEnabled: boolean;
```

- *Type:* boolean

Whether or not the build stage is enabled.

Defaults to true

---

##### `notifyConf`<sup>Optional</sup> <a name="notifyConf" id="cdk-constructs.ThronLambdaSingleEnvPipelineProps.property.notifyConf"></a>

```typescript
public readonly notifyConf: NotifyConf;
```

- *Type:* <a href="#cdk-constructs.NotifyConf">NotifyConf</a>

Configuration for enabling pipeline notifications.

---

### ThronNewRelicContextInjectorOptions <a name="ThronNewRelicContextInjectorOptions" id="cdk-constructs.ThronNewRelicContextInjectorOptions"></a>

#### Initializer <a name="Initializer" id="cdk-constructs.ThronNewRelicContextInjectorOptions.Initializer"></a>

```typescript
import { ThronNewRelicContextInjectorOptions } from 'cdk-constructs'

const thronNewRelicContextInjectorOptions: ThronNewRelicContextInjectorOptions = { ... }
```

#### Properties <a name="Properties" id="Properties"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.ThronNewRelicContextInjectorOptions.property.newRelicConfigOverrides">newRelicConfigOverrides</a></code> | <code><a href="#cdk-constructs.NewRelicLambdaConfigOverrides">NewRelicLambdaConfigOverrides</a></code> | Explicit Overrides for NewRelic Configuration. |

---

##### `newRelicConfigOverrides`<sup>Optional</sup> <a name="newRelicConfigOverrides" id="cdk-constructs.ThronNewRelicContextInjectorOptions.property.newRelicConfigOverrides"></a>

```typescript
public readonly newRelicConfigOverrides: NewRelicLambdaConfigOverrides;
```

- *Type:* <a href="#cdk-constructs.NewRelicLambdaConfigOverrides">NewRelicLambdaConfigOverrides</a>
- *Default:* Empty object with no overrides

Explicit Overrides for NewRelic Configuration.

---

### ThronPipelineBuildProjectProps <a name="ThronPipelineBuildProjectProps" id="cdk-constructs.ThronPipelineBuildProjectProps"></a>

#### Initializer <a name="Initializer" id="cdk-constructs.ThronPipelineBuildProjectProps.Initializer"></a>

```typescript
import { ThronPipelineBuildProjectProps } from 'cdk-constructs'

const thronPipelineBuildProjectProps: ThronPipelineBuildProjectProps = { ... }
```

#### Properties <a name="Properties" id="Properties"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.ThronPipelineBuildProjectProps.property.buildName">buildName</a></code> | <code>string</code> | *No description.* |
| <code><a href="#cdk-constructs.ThronPipelineBuildProjectProps.property.projectPrefix">projectPrefix</a></code> | <code>string</code> | *No description.* |
| <code><a href="#cdk-constructs.ThronPipelineBuildProjectProps.property.buildImage">buildImage</a></code> | <code>aws-cdk-lib.aws_codebuild.IBuildImage</code> | *No description.* |
| <code><a href="#cdk-constructs.ThronPipelineBuildProjectProps.property.buildSpecPath">buildSpecPath</a></code> | <code>string</code> | *No description.* |
| <code><a href="#cdk-constructs.ThronPipelineBuildProjectProps.property.computeType">computeType</a></code> | <code>aws-cdk-lib.aws_codebuild.ComputeType</code> | *No description.* |
| <code><a href="#cdk-constructs.ThronPipelineBuildProjectProps.property.environmentalVariables">environmentalVariables</a></code> | <code>{[ key: string ]: aws-cdk-lib.aws_codebuild.BuildEnvironmentVariable}</code> | *No description.* |

---

##### `buildName`<sup>Required</sup> <a name="buildName" id="cdk-constructs.ThronPipelineBuildProjectProps.property.buildName"></a>

```typescript
public readonly buildName: string;
```

- *Type:* string

---

##### `projectPrefix`<sup>Required</sup> <a name="projectPrefix" id="cdk-constructs.ThronPipelineBuildProjectProps.property.projectPrefix"></a>

```typescript
public readonly projectPrefix: string;
```

- *Type:* string

---

##### `buildImage`<sup>Optional</sup> <a name="buildImage" id="cdk-constructs.ThronPipelineBuildProjectProps.property.buildImage"></a>

```typescript
public readonly buildImage: IBuildImage;
```

- *Type:* aws-cdk-lib.aws_codebuild.IBuildImage

---

##### `buildSpecPath`<sup>Optional</sup> <a name="buildSpecPath" id="cdk-constructs.ThronPipelineBuildProjectProps.property.buildSpecPath"></a>

```typescript
public readonly buildSpecPath: string;
```

- *Type:* string

---

##### `computeType`<sup>Optional</sup> <a name="computeType" id="cdk-constructs.ThronPipelineBuildProjectProps.property.computeType"></a>

```typescript
public readonly computeType: ComputeType;
```

- *Type:* aws-cdk-lib.aws_codebuild.ComputeType

---

##### `environmentalVariables`<sup>Optional</sup> <a name="environmentalVariables" id="cdk-constructs.ThronPipelineBuildProjectProps.property.environmentalVariables"></a>

```typescript
public readonly environmentalVariables: {[ key: string ]: BuildEnvironmentVariable};
```

- *Type:* {[ key: string ]: aws-cdk-lib.aws_codebuild.BuildEnvironmentVariable}

---

### ThronResponseHeaderPolicyProps <a name="ThronResponseHeaderPolicyProps" id="cdk-constructs.ThronResponseHeaderPolicyProps"></a>

#### Initializer <a name="Initializer" id="cdk-constructs.ThronResponseHeaderPolicyProps.Initializer"></a>

```typescript
import { ThronResponseHeaderPolicyProps } from 'cdk-constructs'

const thronResponseHeaderPolicyProps: ThronResponseHeaderPolicyProps = { ... }
```

#### Properties <a name="Properties" id="Properties"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.ThronResponseHeaderPolicyProps.property.additionalCustomHeaders">additionalCustomHeaders</a></code> | <code>aws-cdk-lib.aws_cloudfront.ResponseCustomHeader[]</code> | *No description.* |
| <code><a href="#cdk-constructs.ThronResponseHeaderPolicyProps.property.csp">csp</a></code> | <code>string</code> | Content Security Policy header to set. |

---

##### `additionalCustomHeaders`<sup>Optional</sup> <a name="additionalCustomHeaders" id="cdk-constructs.ThronResponseHeaderPolicyProps.property.additionalCustomHeaders"></a>

```typescript
public readonly additionalCustomHeaders: ResponseCustomHeader[];
```

- *Type:* aws-cdk-lib.aws_cloudfront.ResponseCustomHeader[]

---

##### `csp`<sup>Optional</sup> <a name="csp" id="cdk-constructs.ThronResponseHeaderPolicyProps.property.csp"></a>

```typescript
public readonly csp: string;
```

- *Type:* string

Content Security Policy header to set.

---

### ThronTargetScalingProps <a name="ThronTargetScalingProps" id="cdk-constructs.ThronTargetScalingProps"></a>

#### Initializer <a name="Initializer" id="cdk-constructs.ThronTargetScalingProps.Initializer"></a>

```typescript
import { ThronTargetScalingProps } from 'cdk-constructs'

const thronTargetScalingProps: ThronTargetScalingProps = { ... }
```

#### Properties <a name="Properties" id="Properties"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.ThronTargetScalingProps.property.maxCapacity">maxCapacity</a></code> | <code>number</code> | The maximum value that Application Auto Scaling can use to scale a target during a scaling activity. |
| <code><a href="#cdk-constructs.ThronTargetScalingProps.property.minCapacity">minCapacity</a></code> | <code>number</code> | The minimum value that Application Auto Scaling can use to scale a target during a scaling activity. |
| <code><a href="#cdk-constructs.ThronTargetScalingProps.property.targetValue">targetValue</a></code> | <code>number</code> | The target value for the metric. |
| <code><a href="#cdk-constructs.ThronTargetScalingProps.property.predefinedMetric">predefinedMetric</a></code> | <code>aws-cdk-lib.aws_applicationautoscaling.PredefinedMetric</code> | A predefined metric for application autoscaling. |
| <code><a href="#cdk-constructs.ThronTargetScalingProps.property.scaleInCooldown">scaleInCooldown</a></code> | <code>aws-cdk-lib.Duration</code> | The amount of time after a scale in activity completes before another scale in activity can start. |
| <code><a href="#cdk-constructs.ThronTargetScalingProps.property.scaleOutCooldown">scaleOutCooldown</a></code> | <code>aws-cdk-lib.Duration</code> | The amount of time after a scale in activity completes before another scale in activity can start. |

---

##### `maxCapacity`<sup>Required</sup> <a name="maxCapacity" id="cdk-constructs.ThronTargetScalingProps.property.maxCapacity"></a>

```typescript
public readonly maxCapacity: number;
```

- *Type:* number

The maximum value that Application Auto Scaling can use to scale a target during a scaling activity.

---

##### `minCapacity`<sup>Required</sup> <a name="minCapacity" id="cdk-constructs.ThronTargetScalingProps.property.minCapacity"></a>

```typescript
public readonly minCapacity: number;
```

- *Type:* number

The minimum value that Application Auto Scaling can use to scale a target during a scaling activity.

---

##### `targetValue`<sup>Required</sup> <a name="targetValue" id="cdk-constructs.ThronTargetScalingProps.property.targetValue"></a>

```typescript
public readonly targetValue: number;
```

- *Type:* number

The target value for the metric.

---

##### `predefinedMetric`<sup>Optional</sup> <a name="predefinedMetric" id="cdk-constructs.ThronTargetScalingProps.property.predefinedMetric"></a>

```typescript
public readonly predefinedMetric: PredefinedMetric;
```

- *Type:* aws-cdk-lib.aws_applicationautoscaling.PredefinedMetric

A predefined metric for application autoscaling.

The metric must track utilization. Scaling out will happen if the metric is higher than the target value,
scaling in will happen in the metric is lower than the target value.

---

##### `scaleInCooldown`<sup>Optional</sup> <a name="scaleInCooldown" id="cdk-constructs.ThronTargetScalingProps.property.scaleInCooldown"></a>

```typescript
public readonly scaleInCooldown: Duration;
```

- *Type:* aws-cdk-lib.Duration
- *Default:* Duration.minutes(300)

The amount of time after a scale in activity completes before another scale in activity can start.

---

##### `scaleOutCooldown`<sup>Optional</sup> <a name="scaleOutCooldown" id="cdk-constructs.ThronTargetScalingProps.property.scaleOutCooldown"></a>

```typescript
public readonly scaleOutCooldown: Duration;
```

- *Type:* aws-cdk-lib.Duration
- *Default:* Duration.minutes(90)

The amount of time after a scale in activity completes before another scale in activity can start.

---

### ThronVpcProps <a name="ThronVpcProps" id="cdk-constructs.ThronVpcProps"></a>

ThronVPC Props.

#### Initializer <a name="Initializer" id="cdk-constructs.ThronVpcProps.Initializer"></a>

```typescript
import { ThronVpcProps } from 'cdk-constructs'

const thronVpcProps: ThronVpcProps = { ... }
```

#### Properties <a name="Properties" id="Properties"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.ThronVpcProps.property.gatewayEndpoints">gatewayEndpoints</a></code> | <code>aws-cdk-lib.aws_ec2.GatewayVpcEndpointAwsService[]</code> | Set of gateway endpoints to use in the VPC. |
| <code><a href="#cdk-constructs.ThronVpcProps.property.interfaceEndpoints">interfaceEndpoints</a></code> | <code>aws-cdk-lib.aws_ec2.InterfaceVpcEndpointAwsService[]</code> | Set of interface Endpoints to add to the VPC. |
| <code><a href="#cdk-constructs.ThronVpcProps.property.ipv4Cidr">ipv4Cidr</a></code> | <code>string</code> | IPv4 CIDR to assign to the VPC. |
| <code><a href="#cdk-constructs.ThronVpcProps.property.isNatHA">isNatHA</a></code> | <code>boolean</code> | Whether to use a High Availability NAT configuration. |
| <code><a href="#cdk-constructs.ThronVpcProps.property.prefix">prefix</a></code> | <code>string</code> | Prefix to name all the child resources with. |
| <code><a href="#cdk-constructs.ThronVpcProps.property.subnetsConfigs">subnetsConfigs</a></code> | <code><a href="#cdk-constructs.SubnetConfigProps">SubnetConfigProps</a>[]</code> | Subnet configurations for the VPC. |

---

##### `gatewayEndpoints`<sup>Required</sup> <a name="gatewayEndpoints" id="cdk-constructs.ThronVpcProps.property.gatewayEndpoints"></a>

```typescript
public readonly gatewayEndpoints: GatewayVpcEndpointAwsService[];
```

- *Type:* aws-cdk-lib.aws_ec2.GatewayVpcEndpointAwsService[]

Set of gateway endpoints to use in the VPC.

As they are free, put them all by default! (DYNAMO + S3)

---

##### `interfaceEndpoints`<sup>Required</sup> <a name="interfaceEndpoints" id="cdk-constructs.ThronVpcProps.property.interfaceEndpoints"></a>

```typescript
public readonly interfaceEndpoints: InterfaceVpcEndpointAwsService[];
```

- *Type:* aws-cdk-lib.aws_ec2.InterfaceVpcEndpointAwsService[]

Set of interface Endpoints to add to the VPC.

---

##### `ipv4Cidr`<sup>Required</sup> <a name="ipv4Cidr" id="cdk-constructs.ThronVpcProps.property.ipv4Cidr"></a>

```typescript
public readonly ipv4Cidr: string;
```

- *Type:* string

IPv4 CIDR to assign to the VPC.

---

##### `isNatHA`<sup>Required</sup> <a name="isNatHA" id="cdk-constructs.ThronVpcProps.property.isNatHA"></a>

```typescript
public readonly isNatHA: boolean;
```

- *Type:* boolean

Whether to use a High Availability NAT configuration.

If `true` a NAT will be created in each public subnet, and each private subnets' default route will point to its corresponding az NAT

If `false` a NAT will be created only in the first (alphabetically speaking) zone, and each private subnets' default route will point to it

---

##### `prefix`<sup>Required</sup> <a name="prefix" id="cdk-constructs.ThronVpcProps.property.prefix"></a>

```typescript
public readonly prefix: string;
```

- *Type:* string

Prefix to name all the child resources with.

---

##### `subnetsConfigs`<sup>Required</sup> <a name="subnetsConfigs" id="cdk-constructs.ThronVpcProps.property.subnetsConfigs"></a>

```typescript
public readonly subnetsConfigs: SubnetConfigProps[];
```

- *Type:* <a href="#cdk-constructs.SubnetConfigProps">SubnetConfigProps</a>[]

Subnet configurations for the VPC.

---

## Classes <a name="Classes" id="Classes"></a>

### DockerImageName <a name="DockerImageName" id="cdk-constructs.DockerImageName"></a>

- *Implements:* <a href="#cdk-constructs.IImageName">IImageName</a>

#### Initializers <a name="Initializers" id="cdk-constructs.DockerImageName.Initializer"></a>

```typescript
import { DockerImageName } from 'cdk-constructs'

new DockerImageName(name: string, creds?: string)
```

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.DockerImageName.Initializer.parameter.name">name</a></code> | <code>string</code> | *No description.* |
| <code><a href="#cdk-constructs.DockerImageName.Initializer.parameter.creds">creds</a></code> | <code>string</code> | The credentials of the docker image. |

---

##### `name`<sup>Required</sup> <a name="name" id="cdk-constructs.DockerImageName.Initializer.parameter.name"></a>

- *Type:* string

---

##### `creds`<sup>Optional</sup> <a name="creds" id="cdk-constructs.DockerImageName.Initializer.parameter.creds"></a>

- *Type:* string

The credentials of the docker image.

Format `user:password` or `AWS Secrets Manager secret arn` or `AWS Secrets Manager secret name`

---



#### Properties <a name="Properties" id="Properties"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.DockerImageName.property.uri">uri</a></code> | <code>string</code> | The uri of the docker image. |
| <code><a href="#cdk-constructs.DockerImageName.property.creds">creds</a></code> | <code>string</code> | The credentials of the docker image. |

---

##### `uri`<sup>Required</sup> <a name="uri" id="cdk-constructs.DockerImageName.property.uri"></a>

```typescript
public readonly uri: string;
```

- *Type:* string

The uri of the docker image.

The uri spec follows https://github.com/containers/skopeo

---

##### `creds`<sup>Optional</sup> <a name="creds" id="cdk-constructs.DockerImageName.property.creds"></a>

```typescript
public readonly creds: string;
```

- *Type:* string

The credentials of the docker image.

Format `user:password` or `AWS Secrets Manager secret arn` or `AWS Secrets Manager secret name`

---


### EndpointUtils <a name="EndpointUtils" id="cdk-constructs.EndpointUtils"></a>


#### Static Functions <a name="Static Functions" id="Static Functions"></a>

| **Name** | **Description** |
| --- | --- |
| <code><a href="#cdk-constructs.EndpointUtils.buildInternalServiceRecord">buildInternalServiceRecord</a></code> | Builds the service DNS record from the service infos. |
| <code><a href="#cdk-constructs.EndpointUtils.buildInternalServiceRecordFirstPart">buildInternalServiceRecordFirstPart</a></code> | Builds the service DNS record from the service infos. |
| <code><a href="#cdk-constructs.EndpointUtils.buildPrivateRoutingTokenPrefix">buildPrivateRoutingTokenPrefix</a></code> | Build the routing token prefix for a private endpoint. |
| <code><a href="#cdk-constructs.EndpointUtils.buildPublicRoutingTokenPrefix">buildPublicRoutingTokenPrefix</a></code> | Build the routing token prefix for a public endpoint. |
| <code><a href="#cdk-constructs.EndpointUtils.buildRoutingTokenPrefix">buildRoutingTokenPrefix</a></code> | Build routing token prefix using Thron's conventions. |
| <code><a href="#cdk-constructs.EndpointUtils.buildServiceNameFromRoutingTokenPrefix">buildServiceNameFromRoutingTokenPrefix</a></code> | Builds `serviceName` from routing token. |
| <code><a href="#cdk-constructs.EndpointUtils.isValidRoutingTokenPrefix">isValidRoutingTokenPrefix</a></code> | Validates `routingTokenPrefix` against conventions. |
| <code><a href="#cdk-constructs.EndpointUtils.isValidThronServiceName">isValidThronServiceName</a></code> | Check wether a service name validates against Thron conventions. |
| <code><a href="#cdk-constructs.EndpointUtils.isValidVersion">isValidVersion</a></code> | Validates `version` against conventions. |

---

##### `buildInternalServiceRecord` <a name="buildInternalServiceRecord" id="cdk-constructs.EndpointUtils.buildInternalServiceRecord"></a>

```typescript
import { EndpointUtils } from 'cdk-constructs'

EndpointUtils.buildInternalServiceRecord(serviceName: string, internalDomain: string, sitename: string)
```

Builds the service DNS record from the service infos.

###### `serviceName`<sup>Required</sup> <a name="serviceName" id="cdk-constructs.EndpointUtils.buildInternalServiceRecord.parameter.serviceName"></a>

- *Type:* string

the complete name of the service, i.e `awsd04-view-api-adxsso`.

---

###### `internalDomain`<sup>Required</sup> <a name="internalDomain" id="cdk-constructs.EndpointUtils.buildInternalServiceRecord.parameter.internalDomain"></a>

- *Type:* string

the internal domain, i.e `cdndev.weebo.it`.

---

###### `sitename`<sup>Required</sup> <a name="sitename" id="cdk-constructs.EndpointUtils.buildInternalServiceRecord.parameter.sitename"></a>

- *Type:* string

thron sitename, i.e. `awsd04`.

---

##### `buildInternalServiceRecordFirstPart` <a name="buildInternalServiceRecordFirstPart" id="cdk-constructs.EndpointUtils.buildInternalServiceRecordFirstPart"></a>

```typescript
import { EndpointUtils } from 'cdk-constructs'

EndpointUtils.buildInternalServiceRecordFirstPart(serviceName: string, internalDomain: string, sitename: string)
```

Builds the service DNS record from the service infos.

###### `serviceName`<sup>Required</sup> <a name="serviceName" id="cdk-constructs.EndpointUtils.buildInternalServiceRecordFirstPart.parameter.serviceName"></a>

- *Type:* string

the complete name of the service, i.e `awsd04-view-api-adxsso`.

---

###### `internalDomain`<sup>Required</sup> <a name="internalDomain" id="cdk-constructs.EndpointUtils.buildInternalServiceRecordFirstPart.parameter.internalDomain"></a>

- *Type:* string

the internal domain, i.e `cdndev.weebo.it`.

---

###### `sitename`<sup>Required</sup> <a name="sitename" id="cdk-constructs.EndpointUtils.buildInternalServiceRecordFirstPart.parameter.sitename"></a>

- *Type:* string

thron sitename, i.e. `awsd04`.

---

##### `buildPrivateRoutingTokenPrefix` <a name="buildPrivateRoutingTokenPrefix" id="cdk-constructs.EndpointUtils.buildPrivateRoutingTokenPrefix"></a>

```typescript
import { EndpointUtils } from 'cdk-constructs'

EndpointUtils.buildPrivateRoutingTokenPrefix(serviceName: string, version: number)
```

Build the routing token prefix for a private endpoint.

###### `serviceName`<sup>Required</sup> <a name="serviceName" id="cdk-constructs.EndpointUtils.buildPrivateRoutingTokenPrefix.parameter.serviceName"></a>

- *Type:* string

---

###### `version`<sup>Required</sup> <a name="version" id="cdk-constructs.EndpointUtils.buildPrivateRoutingTokenPrefix.parameter.version"></a>

- *Type:* number

---

##### `buildPublicRoutingTokenPrefix` <a name="buildPublicRoutingTokenPrefix" id="cdk-constructs.EndpointUtils.buildPublicRoutingTokenPrefix"></a>

```typescript
import { EndpointUtils } from 'cdk-constructs'

EndpointUtils.buildPublicRoutingTokenPrefix(serviceName: string, version: number)
```

Build the routing token prefix for a public endpoint.

###### `serviceName`<sup>Required</sup> <a name="serviceName" id="cdk-constructs.EndpointUtils.buildPublicRoutingTokenPrefix.parameter.serviceName"></a>

- *Type:* string

---

###### `version`<sup>Required</sup> <a name="version" id="cdk-constructs.EndpointUtils.buildPublicRoutingTokenPrefix.parameter.version"></a>

- *Type:* number

---

##### `buildRoutingTokenPrefix` <a name="buildRoutingTokenPrefix" id="cdk-constructs.EndpointUtils.buildRoutingTokenPrefix"></a>

```typescript
import { EndpointUtils } from 'cdk-constructs'

EndpointUtils.buildRoutingTokenPrefix(serviceName: string, version: number, visibility: EndpointVisibility)
```

Build routing token prefix using Thron's conventions.

###### `serviceName`<sup>Required</sup> <a name="serviceName" id="cdk-constructs.EndpointUtils.buildRoutingTokenPrefix.parameter.serviceName"></a>

- *Type:* string

---

###### `version`<sup>Required</sup> <a name="version" id="cdk-constructs.EndpointUtils.buildRoutingTokenPrefix.parameter.version"></a>

- *Type:* number

---

###### `visibility`<sup>Required</sup> <a name="visibility" id="cdk-constructs.EndpointUtils.buildRoutingTokenPrefix.parameter.visibility"></a>

- *Type:* <a href="#cdk-constructs.EndpointVisibility">EndpointVisibility</a>

---

##### `buildServiceNameFromRoutingTokenPrefix` <a name="buildServiceNameFromRoutingTokenPrefix" id="cdk-constructs.EndpointUtils.buildServiceNameFromRoutingTokenPrefix"></a>

```typescript
import { EndpointUtils } from 'cdk-constructs'

EndpointUtils.buildServiceNameFromRoutingTokenPrefix(routingTokenPrefix: string, serviceGroup: ServiceGroup)
```

Builds `serviceName` from routing token.

###### `routingTokenPrefix`<sup>Required</sup> <a name="routingTokenPrefix" id="cdk-constructs.EndpointUtils.buildServiceNameFromRoutingTokenPrefix.parameter.routingTokenPrefix"></a>

- *Type:* string

service routing token.

---

###### `serviceGroup`<sup>Required</sup> <a name="serviceGroup" id="cdk-constructs.EndpointUtils.buildServiceNameFromRoutingTokenPrefix.parameter.serviceGroup"></a>

- *Type:* <a href="#cdk-constructs.ServiceGroup">ServiceGroup</a>

service group.

---

##### `isValidRoutingTokenPrefix` <a name="isValidRoutingTokenPrefix" id="cdk-constructs.EndpointUtils.isValidRoutingTokenPrefix"></a>

```typescript
import { EndpointUtils } from 'cdk-constructs'

EndpointUtils.isValidRoutingTokenPrefix(routingTokenPrefix: string)
```

Validates `routingTokenPrefix` against conventions.

###### `routingTokenPrefix`<sup>Required</sup> <a name="routingTokenPrefix" id="cdk-constructs.EndpointUtils.isValidRoutingTokenPrefix.parameter.routingTokenPrefix"></a>

- *Type:* string

routing token prefix to validate.

---

##### `isValidThronServiceName` <a name="isValidThronServiceName" id="cdk-constructs.EndpointUtils.isValidThronServiceName"></a>

```typescript
import { EndpointUtils } from 'cdk-constructs'

EndpointUtils.isValidThronServiceName(serviceName: string)
```

Check wether a service name validates against Thron conventions.

###### `serviceName`<sup>Required</sup> <a name="serviceName" id="cdk-constructs.EndpointUtils.isValidThronServiceName.parameter.serviceName"></a>

- *Type:* string

---

##### `isValidVersion` <a name="isValidVersion" id="cdk-constructs.EndpointUtils.isValidVersion"></a>

```typescript
import { EndpointUtils } from 'cdk-constructs'

EndpointUtils.isValidVersion(version?: number)
```

Validates `version` against conventions.

###### `version`<sup>Optional</sup> <a name="version" id="cdk-constructs.EndpointUtils.isValidVersion.parameter.version"></a>

- *Type:* number

---



### S3ArchiveName <a name="S3ArchiveName" id="cdk-constructs.S3ArchiveName"></a>

- *Implements:* <a href="#cdk-constructs.IImageName">IImageName</a>

#### Initializers <a name="Initializers" id="cdk-constructs.S3ArchiveName.Initializer"></a>

```typescript
import { S3ArchiveName } from 'cdk-constructs'

new S3ArchiveName(p: string, ref?: string, creds?: string)
```

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.S3ArchiveName.Initializer.parameter.p">p</a></code> | <code>string</code> | *No description.* |
| <code><a href="#cdk-constructs.S3ArchiveName.Initializer.parameter.ref">ref</a></code> | <code>string</code> | *No description.* |
| <code><a href="#cdk-constructs.S3ArchiveName.Initializer.parameter.creds">creds</a></code> | <code>string</code> | The credentials of the docker image. |

---

##### `p`<sup>Required</sup> <a name="p" id="cdk-constructs.S3ArchiveName.Initializer.parameter.p"></a>

- *Type:* string

---

##### `ref`<sup>Optional</sup> <a name="ref" id="cdk-constructs.S3ArchiveName.Initializer.parameter.ref"></a>

- *Type:* string

---

##### `creds`<sup>Optional</sup> <a name="creds" id="cdk-constructs.S3ArchiveName.Initializer.parameter.creds"></a>

- *Type:* string

The credentials of the docker image.

Format `user:password` or `AWS Secrets Manager secret arn` or `AWS Secrets Manager secret name`

---



#### Properties <a name="Properties" id="Properties"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.S3ArchiveName.property.uri">uri</a></code> | <code>string</code> | The uri of the docker image. |
| <code><a href="#cdk-constructs.S3ArchiveName.property.creds">creds</a></code> | <code>string</code> | The credentials of the docker image. |

---

##### `uri`<sup>Required</sup> <a name="uri" id="cdk-constructs.S3ArchiveName.property.uri"></a>

```typescript
public readonly uri: string;
```

- *Type:* string

The uri of the docker image.

The uri spec follows https://github.com/containers/skopeo

---

##### `creds`<sup>Optional</sup> <a name="creds" id="cdk-constructs.S3ArchiveName.property.creds"></a>

```typescript
public readonly creds: string;
```

- *Type:* string

The credentials of the docker image.

Format `user:password` or `AWS Secrets Manager secret arn` or `AWS Secrets Manager secret name`

---


### ThronApiGatewayUtils <a name="ThronApiGatewayUtils" id="cdk-constructs.ThronApiGatewayUtils"></a>


#### Static Functions <a name="Static Functions" id="Static Functions"></a>

| **Name** | **Description** |
| --- | --- |
| <code><a href="#cdk-constructs.ThronApiGatewayUtils.apigwMainIdSsmParam">apigwMainIdSsmParam</a></code> | *No description.* |
| <code><a href="#cdk-constructs.ThronApiGatewayUtils.apigwVpceDnsSsmParam">apigwVpceDnsSsmParam</a></code> | *No description.* |
| <code><a href="#cdk-constructs.ThronApiGatewayUtils.apigwVpceIdSsmParam">apigwVpceIdSsmParam</a></code> | *No description.* |
| <code><a href="#cdk-constructs.ThronApiGatewayUtils.certificateIdArnSsmParam">certificateIdArnSsmParam</a></code> | *No description.* |
| <code><a href="#cdk-constructs.ThronApiGatewayUtils.sanitizeId">sanitizeId</a></code> | *No description.* |

---

##### `apigwMainIdSsmParam` <a name="apigwMainIdSsmParam" id="cdk-constructs.ThronApiGatewayUtils.apigwMainIdSsmParam"></a>

```typescript
import { ThronApiGatewayUtils } from 'cdk-constructs'

ThronApiGatewayUtils.apigwMainIdSsmParam(thronSitename: string)
```

###### `thronSitename`<sup>Required</sup> <a name="thronSitename" id="cdk-constructs.ThronApiGatewayUtils.apigwMainIdSsmParam.parameter.thronSitename"></a>

- *Type:* string

---

##### `apigwVpceDnsSsmParam` <a name="apigwVpceDnsSsmParam" id="cdk-constructs.ThronApiGatewayUtils.apigwVpceDnsSsmParam"></a>

```typescript
import { ThronApiGatewayUtils } from 'cdk-constructs'

ThronApiGatewayUtils.apigwVpceDnsSsmParam(thronSitename: string)
```

###### `thronSitename`<sup>Required</sup> <a name="thronSitename" id="cdk-constructs.ThronApiGatewayUtils.apigwVpceDnsSsmParam.parameter.thronSitename"></a>

- *Type:* string

---

##### `apigwVpceIdSsmParam` <a name="apigwVpceIdSsmParam" id="cdk-constructs.ThronApiGatewayUtils.apigwVpceIdSsmParam"></a>

```typescript
import { ThronApiGatewayUtils } from 'cdk-constructs'

ThronApiGatewayUtils.apigwVpceIdSsmParam(thronSitename: string)
```

###### `thronSitename`<sup>Required</sup> <a name="thronSitename" id="cdk-constructs.ThronApiGatewayUtils.apigwVpceIdSsmParam.parameter.thronSitename"></a>

- *Type:* string

---

##### `certificateIdArnSsmParam` <a name="certificateIdArnSsmParam" id="cdk-constructs.ThronApiGatewayUtils.certificateIdArnSsmParam"></a>

```typescript
import { ThronApiGatewayUtils } from 'cdk-constructs'

ThronApiGatewayUtils.certificateIdArnSsmParam(thronSitename: string)
```

###### `thronSitename`<sup>Required</sup> <a name="thronSitename" id="cdk-constructs.ThronApiGatewayUtils.certificateIdArnSsmParam.parameter.thronSitename"></a>

- *Type:* string

---

##### `sanitizeId` <a name="sanitizeId" id="cdk-constructs.ThronApiGatewayUtils.sanitizeId"></a>

```typescript
import { ThronApiGatewayUtils } from 'cdk-constructs'

ThronApiGatewayUtils.sanitizeId(id: string)
```

###### `id`<sup>Required</sup> <a name="id" id="cdk-constructs.ThronApiGatewayUtils.sanitizeId.parameter.id"></a>

- *Type:* string

---



### ThronEnvironment <a name="ThronEnvironment" id="cdk-constructs.ThronEnvironment"></a>

#### Initializers <a name="Initializers" id="cdk-constructs.ThronEnvironment.Initializer"></a>

```typescript
import { ThronEnvironment } from 'cdk-constructs'

new ThronEnvironment()
```

| **Name** | **Type** | **Description** |
| --- | --- | --- |

---




#### Constants <a name="Constants" id="Constants"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.ThronEnvironment.property.BETA">BETA</a></code> | <code>string</code> | *No description.* |
| <code><a href="#cdk-constructs.ThronEnvironment.property.DEVELOPMENT">DEVELOPMENT</a></code> | <code>string</code> | *No description.* |
| <code><a href="#cdk-constructs.ThronEnvironment.property.PRODUCTION">PRODUCTION</a></code> | <code>string</code> | *No description.* |
| <code><a href="#cdk-constructs.ThronEnvironment.property.QUALITY">QUALITY</a></code> | <code>string</code> | *No description.* |

---

##### `BETA`<sup>Required</sup> <a name="BETA" id="cdk-constructs.ThronEnvironment.property.BETA"></a>

```typescript
public readonly BETA: string;
```

- *Type:* string

---

##### `DEVELOPMENT`<sup>Required</sup> <a name="DEVELOPMENT" id="cdk-constructs.ThronEnvironment.property.DEVELOPMENT"></a>

```typescript
public readonly DEVELOPMENT: string;
```

- *Type:* string

---

##### `PRODUCTION`<sup>Required</sup> <a name="PRODUCTION" id="cdk-constructs.ThronEnvironment.property.PRODUCTION"></a>

```typescript
public readonly PRODUCTION: string;
```

- *Type:* string

---

##### `QUALITY`<sup>Required</sup> <a name="QUALITY" id="cdk-constructs.ThronEnvironment.property.QUALITY"></a>

```typescript
public readonly QUALITY: string;
```

- *Type:* string

---

### ThronHealthCheck <a name="ThronHealthCheck" id="cdk-constructs.ThronHealthCheck"></a>

#### Initializers <a name="Initializers" id="cdk-constructs.ThronHealthCheck.Initializer"></a>

```typescript
import { ThronHealthCheck } from 'cdk-constructs'

new ThronHealthCheck()
```

| **Name** | **Type** | **Description** |
| --- | --- | --- |

---


#### Static Functions <a name="Static Functions" id="Static Functions"></a>

| **Name** | **Description** |
| --- | --- |
| <code><a href="#cdk-constructs.ThronHealthCheck.default">default</a></code> | *No description.* |
| <code><a href="#cdk-constructs.ThronHealthCheck.defaultWithOverrides">defaultWithOverrides</a></code> | *No description.* |

---

##### `default` <a name="default" id="cdk-constructs.ThronHealthCheck.default"></a>

```typescript
import { ThronHealthCheck } from 'cdk-constructs'

ThronHealthCheck.default()
```

##### `defaultWithOverrides` <a name="defaultWithOverrides" id="cdk-constructs.ThronHealthCheck.defaultWithOverrides"></a>

```typescript
import { ThronHealthCheck } from 'cdk-constructs'

ThronHealthCheck.defaultWithOverrides(props: ThronHealthCheckOverride)
```

###### `props`<sup>Required</sup> <a name="props" id="cdk-constructs.ThronHealthCheck.defaultWithOverrides.parameter.props"></a>

- *Type:* <a href="#cdk-constructs.ThronHealthCheckOverride">ThronHealthCheckOverride</a>

---



### ThronLambdaSingleEnvPipelineBuilder <a name="ThronLambdaSingleEnvPipelineBuilder" id="cdk-constructs.ThronLambdaSingleEnvPipelineBuilder"></a>

Builder Class for {@link ThronLambdaSingleEnvPipeline}.

#### Initializers <a name="Initializers" id="cdk-constructs.ThronLambdaSingleEnvPipelineBuilder.Initializer"></a>

```typescript
import { ThronLambdaSingleEnvPipelineBuilder } from 'cdk-constructs'

new ThronLambdaSingleEnvPipelineBuilder()
```

| **Name** | **Type** | **Description** |
| --- | --- | --- |

---

#### Methods <a name="Methods" id="Methods"></a>

| **Name** | **Description** |
| --- | --- |
| <code><a href="#cdk-constructs.ThronLambdaSingleEnvPipelineBuilder.buildPipeline">buildPipeline</a></code> | *No description.* |
| <code><a href="#cdk-constructs.ThronLambdaSingleEnvPipelineBuilder.withArtifactBucket">withArtifactBucket</a></code> | *No description.* |
| <code><a href="#cdk-constructs.ThronLambdaSingleEnvPipelineBuilder.withBuildDisabled">withBuildDisabled</a></code> | *No description.* |
| <code><a href="#cdk-constructs.ThronLambdaSingleEnvPipelineBuilder.withDefaultBuildStepConfig">withDefaultBuildStepConfig</a></code> | *No description.* |
| <code><a href="#cdk-constructs.ThronLambdaSingleEnvPipelineBuilder.withDefaultDeployStepConfig">withDefaultDeployStepConfig</a></code> | *No description.* |
| <code><a href="#cdk-constructs.ThronLambdaSingleEnvPipelineBuilder.withDefaultStepConfig">withDefaultStepConfig</a></code> | *No description.* |
| <code><a href="#cdk-constructs.ThronLambdaSingleEnvPipelineBuilder.withDefaultTestStepConfig">withDefaultTestStepConfig</a></code> | *No description.* |
| <code><a href="#cdk-constructs.ThronLambdaSingleEnvPipelineBuilder.withDeployEnvironment">withDeployEnvironment</a></code> | *No description.* |
| <code><a href="#cdk-constructs.ThronLambdaSingleEnvPipelineBuilder.withLambda">withLambda</a></code> | *No description.* |
| <code><a href="#cdk-constructs.ThronLambdaSingleEnvPipelineBuilder.withNotifyConfig">withNotifyConfig</a></code> | *No description.* |
| <code><a href="#cdk-constructs.ThronLambdaSingleEnvPipelineBuilder.withSourceConfiguration">withSourceConfiguration</a></code> | *No description.* |
| <code><a href="#cdk-constructs.ThronLambdaSingleEnvPipelineBuilder.withTestStep">withTestStep</a></code> | *No description.* |

---

##### `buildPipeline` <a name="buildPipeline" id="cdk-constructs.ThronLambdaSingleEnvPipelineBuilder.buildPipeline"></a>

```typescript
public buildPipeline(scope: Construct, id: string, prefix: string): ThronLambdaSingleEnvPipeline
```

###### `scope`<sup>Required</sup> <a name="scope" id="cdk-constructs.ThronLambdaSingleEnvPipelineBuilder.buildPipeline.parameter.scope"></a>

- *Type:* constructs.Construct

---

###### `id`<sup>Required</sup> <a name="id" id="cdk-constructs.ThronLambdaSingleEnvPipelineBuilder.buildPipeline.parameter.id"></a>

- *Type:* string

---

###### `prefix`<sup>Required</sup> <a name="prefix" id="cdk-constructs.ThronLambdaSingleEnvPipelineBuilder.buildPipeline.parameter.prefix"></a>

- *Type:* string

---

##### `withArtifactBucket` <a name="withArtifactBucket" id="cdk-constructs.ThronLambdaSingleEnvPipelineBuilder.withArtifactBucket"></a>

```typescript
public withArtifactBucket(artifactBucket: IBucket): ThronLambdaSingleEnvPipelineBuilder
```

###### `artifactBucket`<sup>Required</sup> <a name="artifactBucket" id="cdk-constructs.ThronLambdaSingleEnvPipelineBuilder.withArtifactBucket.parameter.artifactBucket"></a>

- *Type:* aws-cdk-lib.aws_s3.IBucket

---

##### `withBuildDisabled` <a name="withBuildDisabled" id="cdk-constructs.ThronLambdaSingleEnvPipelineBuilder.withBuildDisabled"></a>

```typescript
public withBuildDisabled(): ThronLambdaSingleEnvPipelineBuilder
```

##### `withDefaultBuildStepConfig` <a name="withDefaultBuildStepConfig" id="cdk-constructs.ThronLambdaSingleEnvPipelineBuilder.withDefaultBuildStepConfig"></a>

```typescript
public withDefaultBuildStepConfig(stepConfig: StepConfig): ThronLambdaSingleEnvPipelineBuilder
```

###### `stepConfig`<sup>Required</sup> <a name="stepConfig" id="cdk-constructs.ThronLambdaSingleEnvPipelineBuilder.withDefaultBuildStepConfig.parameter.stepConfig"></a>

- *Type:* <a href="#cdk-constructs.StepConfig">StepConfig</a>

---

##### `withDefaultDeployStepConfig` <a name="withDefaultDeployStepConfig" id="cdk-constructs.ThronLambdaSingleEnvPipelineBuilder.withDefaultDeployStepConfig"></a>

```typescript
public withDefaultDeployStepConfig(stepConfig: StepConfig): ThronLambdaSingleEnvPipelineBuilder
```

###### `stepConfig`<sup>Required</sup> <a name="stepConfig" id="cdk-constructs.ThronLambdaSingleEnvPipelineBuilder.withDefaultDeployStepConfig.parameter.stepConfig"></a>

- *Type:* <a href="#cdk-constructs.StepConfig">StepConfig</a>

---

##### `withDefaultStepConfig` <a name="withDefaultStepConfig" id="cdk-constructs.ThronLambdaSingleEnvPipelineBuilder.withDefaultStepConfig"></a>

```typescript
public withDefaultStepConfig(stepConfig: StepConfig): ThronLambdaSingleEnvPipelineBuilder
```

###### `stepConfig`<sup>Required</sup> <a name="stepConfig" id="cdk-constructs.ThronLambdaSingleEnvPipelineBuilder.withDefaultStepConfig.parameter.stepConfig"></a>

- *Type:* <a href="#cdk-constructs.StepConfig">StepConfig</a>

---

##### `withDefaultTestStepConfig` <a name="withDefaultTestStepConfig" id="cdk-constructs.ThronLambdaSingleEnvPipelineBuilder.withDefaultTestStepConfig"></a>

```typescript
public withDefaultTestStepConfig(stepConfig: StepConfig): ThronLambdaSingleEnvPipelineBuilder
```

###### `stepConfig`<sup>Required</sup> <a name="stepConfig" id="cdk-constructs.ThronLambdaSingleEnvPipelineBuilder.withDefaultTestStepConfig.parameter.stepConfig"></a>

- *Type:* <a href="#cdk-constructs.StepConfig">StepConfig</a>

---

##### `withDeployEnvironment` <a name="withDeployEnvironment" id="cdk-constructs.ThronLambdaSingleEnvPipelineBuilder.withDeployEnvironment"></a>

```typescript
public withDeployEnvironment(deployConfig: DeployConfig): ThronLambdaSingleEnvPipelineBuilder
```

###### `deployConfig`<sup>Required</sup> <a name="deployConfig" id="cdk-constructs.ThronLambdaSingleEnvPipelineBuilder.withDeployEnvironment.parameter.deployConfig"></a>

- *Type:* <a href="#cdk-constructs.DeployConfig">DeployConfig</a>

---

##### `withLambda` <a name="withLambda" id="cdk-constructs.ThronLambdaSingleEnvPipelineBuilder.withLambda"></a>

```typescript
public withLambda(lambdaId: string, destinationEcrRepository: Repository, stepConfOverrides?: StepConfig): ThronLambdaSingleEnvPipelineBuilder
```

###### `lambdaId`<sup>Required</sup> <a name="lambdaId" id="cdk-constructs.ThronLambdaSingleEnvPipelineBuilder.withLambda.parameter.lambdaId"></a>

- *Type:* string

---

###### `destinationEcrRepository`<sup>Required</sup> <a name="destinationEcrRepository" id="cdk-constructs.ThronLambdaSingleEnvPipelineBuilder.withLambda.parameter.destinationEcrRepository"></a>

- *Type:* aws-cdk-lib.aws_ecr.Repository

---

###### `stepConfOverrides`<sup>Optional</sup> <a name="stepConfOverrides" id="cdk-constructs.ThronLambdaSingleEnvPipelineBuilder.withLambda.parameter.stepConfOverrides"></a>

- *Type:* <a href="#cdk-constructs.StepConfig">StepConfig</a>

---

##### `withNotifyConfig` <a name="withNotifyConfig" id="cdk-constructs.ThronLambdaSingleEnvPipelineBuilder.withNotifyConfig"></a>

```typescript
public withNotifyConfig(notifyConf: NotifyConf): ThronLambdaSingleEnvPipelineBuilder
```

###### `notifyConf`<sup>Required</sup> <a name="notifyConf" id="cdk-constructs.ThronLambdaSingleEnvPipelineBuilder.withNotifyConfig.parameter.notifyConf"></a>

- *Type:* <a href="#cdk-constructs.NotifyConf">NotifyConf</a>

---

##### `withSourceConfiguration` <a name="withSourceConfiguration" id="cdk-constructs.ThronLambdaSingleEnvPipelineBuilder.withSourceConfiguration"></a>

```typescript
public withSourceConfiguration(sourceConfig: ThronLambdaSingleEnvPipelineCodeCommitProps): ThronLambdaSingleEnvPipelineBuilder
```

###### `sourceConfig`<sup>Required</sup> <a name="sourceConfig" id="cdk-constructs.ThronLambdaSingleEnvPipelineBuilder.withSourceConfiguration.parameter.sourceConfig"></a>

- *Type:* <a href="#cdk-constructs.ThronLambdaSingleEnvPipelineCodeCommitProps">ThronLambdaSingleEnvPipelineCodeCommitProps</a>

---

##### `withTestStep` <a name="withTestStep" id="cdk-constructs.ThronLambdaSingleEnvPipelineBuilder.withTestStep"></a>

```typescript
public withTestStep(testId: string, stepConfOverrides?: StepConfig): ThronLambdaSingleEnvPipelineBuilder
```

###### `testId`<sup>Required</sup> <a name="testId" id="cdk-constructs.ThronLambdaSingleEnvPipelineBuilder.withTestStep.parameter.testId"></a>

- *Type:* string

---

###### `stepConfOverrides`<sup>Optional</sup> <a name="stepConfOverrides" id="cdk-constructs.ThronLambdaSingleEnvPipelineBuilder.withTestStep.parameter.stepConfOverrides"></a>

- *Type:* <a href="#cdk-constructs.StepConfig">StepConfig</a>

---



#### Constants <a name="Constants" id="Constants"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.ThronLambdaSingleEnvPipelineBuilder.property.DefaultStepConfig">DefaultStepConfig</a></code> | <code><a href="#cdk-constructs.StepConfig">StepConfig</a></code> | *No description.* |

---

##### `DefaultStepConfig`<sup>Required</sup> <a name="DefaultStepConfig" id="cdk-constructs.ThronLambdaSingleEnvPipelineBuilder.property.DefaultStepConfig"></a>

```typescript
public readonly DefaultStepConfig: StepConfig;
```

- *Type:* <a href="#cdk-constructs.StepConfig">StepConfig</a>

---

## Protocols <a name="Protocols" id="Protocols"></a>

### IImageName <a name="IImageName" id="cdk-constructs.IImageName"></a>

- *Implemented By:* <a href="#cdk-constructs.DockerImageName">DockerImageName</a>, <a href="#cdk-constructs.S3ArchiveName">S3ArchiveName</a>, <a href="#cdk-constructs.IImageName">IImageName</a>


#### Properties <a name="Properties" id="Properties"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.IImageName.property.uri">uri</a></code> | <code>string</code> | The uri of the docker image. |
| <code><a href="#cdk-constructs.IImageName.property.creds">creds</a></code> | <code>string</code> | The credentials of the docker image. |

---

##### `uri`<sup>Required</sup> <a name="uri" id="cdk-constructs.IImageName.property.uri"></a>

```typescript
public readonly uri: string;
```

- *Type:* string

The uri of the docker image.

The uri spec follows https://github.com/containers/skopeo

---

##### `creds`<sup>Optional</sup> <a name="creds" id="cdk-constructs.IImageName.property.creds"></a>

```typescript
public readonly creds: string;
```

- *Type:* string

The credentials of the docker image.

Format `user:password` or `AWS Secrets Manager secret arn` or `AWS Secrets Manager secret name`

---

## Enums <a name="Enums" id="Enums"></a>

### AvailabilityZone <a name="AvailabilityZone" id="cdk-constructs.AvailabilityZone"></a>

Enum with all the AZ you may use in a region.

#### Members <a name="Members" id="Members"></a>

| **Name** | **Description** |
| --- | --- |
| <code><a href="#cdk-constructs.AvailabilityZone.A">A</a></code> | *No description.* |
| <code><a href="#cdk-constructs.AvailabilityZone.B">B</a></code> | *No description.* |
| <code><a href="#cdk-constructs.AvailabilityZone.C">C</a></code> | *No description.* |
| <code><a href="#cdk-constructs.AvailabilityZone.D">D</a></code> | *No description.* |

---

##### `A` <a name="A" id="cdk-constructs.AvailabilityZone.A"></a>

---


##### `B` <a name="B" id="cdk-constructs.AvailabilityZone.B"></a>

---


##### `C` <a name="C" id="cdk-constructs.AvailabilityZone.C"></a>

---


##### `D` <a name="D" id="cdk-constructs.AvailabilityZone.D"></a>

---


### ClusterOption <a name="ClusterOption" id="cdk-constructs.ClusterOption"></a>

#### Members <a name="Members" id="Members"></a>

| **Name** | **Description** |
| --- | --- |
| <code><a href="#cdk-constructs.ClusterOption.CORE_MAIN">CORE_MAIN</a></code> | *No description.* |
| <code><a href="#cdk-constructs.ClusterOption.ECS_MANAGEMENT">ECS_MANAGEMENT</a></code> | *No description.* |
| <code><a href="#cdk-constructs.ClusterOption.THE_SHIRE">THE_SHIRE</a></code> | *No description.* |
| <code><a href="#cdk-constructs.ClusterOption.VALINOR">VALINOR</a></code> | *No description.* |

---

##### `CORE_MAIN` <a name="CORE_MAIN" id="cdk-constructs.ClusterOption.CORE_MAIN"></a>

---


##### `ECS_MANAGEMENT` <a name="ECS_MANAGEMENT" id="cdk-constructs.ClusterOption.ECS_MANAGEMENT"></a>

---


##### `THE_SHIRE` <a name="THE_SHIRE" id="cdk-constructs.ClusterOption.THE_SHIRE"></a>

---


##### `VALINOR` <a name="VALINOR" id="cdk-constructs.ClusterOption.VALINOR"></a>

---


### EndpointVisibility <a name="EndpointVisibility" id="cdk-constructs.EndpointVisibility"></a>

#### Members <a name="Members" id="Members"></a>

| **Name** | **Description** |
| --- | --- |
| <code><a href="#cdk-constructs.EndpointVisibility.PUBLIC">PUBLIC</a></code> | *No description.* |
| <code><a href="#cdk-constructs.EndpointVisibility.PRIVATE">PRIVATE</a></code> | *No description.* |

---

##### `PUBLIC` <a name="PUBLIC" id="cdk-constructs.EndpointVisibility.PUBLIC"></a>

---


##### `PRIVATE` <a name="PRIVATE" id="cdk-constructs.EndpointVisibility.PRIVATE"></a>

---


### NewRelicIgnoreExtensionChecksOption <a name="NewRelicIgnoreExtensionChecksOption" id="cdk-constructs.NewRelicIgnoreExtensionChecksOption"></a>

#### Members <a name="Members" id="Members"></a>

| **Name** | **Description** |
| --- | --- |
| <code><a href="#cdk-constructs.NewRelicIgnoreExtensionChecksOption.ALL">ALL</a></code> | *No description.* |
| <code><a href="#cdk-constructs.NewRelicIgnoreExtensionChecksOption.AGENT">AGENT</a></code> | *No description.* |
| <code><a href="#cdk-constructs.NewRelicIgnoreExtensionChecksOption.HANDLER">HANDLER</a></code> | *No description.* |
| <code><a href="#cdk-constructs.NewRelicIgnoreExtensionChecksOption.SANITY">SANITY</a></code> | *No description.* |
| <code><a href="#cdk-constructs.NewRelicIgnoreExtensionChecksOption.VENDOR">VENDOR</a></code> | *No description.* |
| <code><a href="#cdk-constructs.NewRelicIgnoreExtensionChecksOption.FALSE">FALSE</a></code> | *No description.* |

---

##### `ALL` <a name="ALL" id="cdk-constructs.NewRelicIgnoreExtensionChecksOption.ALL"></a>

---


##### `AGENT` <a name="AGENT" id="cdk-constructs.NewRelicIgnoreExtensionChecksOption.AGENT"></a>

---


##### `HANDLER` <a name="HANDLER" id="cdk-constructs.NewRelicIgnoreExtensionChecksOption.HANDLER"></a>

---


##### `SANITY` <a name="SANITY" id="cdk-constructs.NewRelicIgnoreExtensionChecksOption.SANITY"></a>

---


##### `VENDOR` <a name="VENDOR" id="cdk-constructs.NewRelicIgnoreExtensionChecksOption.VENDOR"></a>

---


##### `FALSE` <a name="FALSE" id="cdk-constructs.NewRelicIgnoreExtensionChecksOption.FALSE"></a>

---


### PipelineCapability <a name="PipelineCapability" id="cdk-constructs.PipelineCapability"></a>

#### Members <a name="Members" id="Members"></a>

| **Name** | **Description** |
| --- | --- |
| <code><a href="#cdk-constructs.PipelineCapability.BUILD">BUILD</a></code> | Enable BUILD stage in the pipeline. |
| <code><a href="#cdk-constructs.PipelineCapability.TEST">TEST</a></code> | Enable TEST stage in the pipeline. |
| <code><a href="#cdk-constructs.PipelineCapability.NOTIFY_ON_START">NOTIFY_ON_START</a></code> | Enable pipeline notification when the pipeline starts, both manually or via a new commit. |
| <code><a href="#cdk-constructs.PipelineCapability.NOTIFY_ON_FAIL">NOTIFY_ON_FAIL</a></code> | Enable pipeline notification when the pipeline fails. |
| <code><a href="#cdk-constructs.PipelineCapability.NOTIFY_ON_SUCCESS">NOTIFY_ON_SUCCESS</a></code> | Enable pipeline notification when the pipeline succeeds. |

---

##### `BUILD` <a name="BUILD" id="cdk-constructs.PipelineCapability.BUILD"></a>

Enable BUILD stage in the pipeline.

---


##### `TEST` <a name="TEST" id="cdk-constructs.PipelineCapability.TEST"></a>

Enable TEST stage in the pipeline.

---


##### `NOTIFY_ON_START` <a name="NOTIFY_ON_START" id="cdk-constructs.PipelineCapability.NOTIFY_ON_START"></a>

Enable pipeline notification when the pipeline starts, both manually or via a new commit.

---


##### `NOTIFY_ON_FAIL` <a name="NOTIFY_ON_FAIL" id="cdk-constructs.PipelineCapability.NOTIFY_ON_FAIL"></a>

Enable pipeline notification when the pipeline fails.

---


##### `NOTIFY_ON_SUCCESS` <a name="NOTIFY_ON_SUCCESS" id="cdk-constructs.PipelineCapability.NOTIFY_ON_SUCCESS"></a>

Enable pipeline notification when the pipeline succeeds.

---


### ServiceGroup <a name="ServiceGroup" id="cdk-constructs.ServiceGroup"></a>

#### Members <a name="Members" id="Members"></a>

| **Name** | **Description** |
| --- | --- |
| <code><a href="#cdk-constructs.ServiceGroup.PRODUCT">PRODUCT</a></code> | *No description.* |
| <code><a href="#cdk-constructs.ServiceGroup.VIEW">VIEW</a></code> | *No description.* |

---

##### `PRODUCT` <a name="PRODUCT" id="cdk-constructs.ServiceGroup.PRODUCT"></a>

---


##### `VIEW` <a name="VIEW" id="cdk-constructs.ServiceGroup.VIEW"></a>

---


### SubnetType <a name="SubnetType" id="cdk-constructs.SubnetType"></a>

Attribute indicating whether a Subnet is public or private.

#### Members <a name="Members" id="Members"></a>

| **Name** | **Description** |
| --- | --- |
| <code><a href="#cdk-constructs.SubnetType.PUBLIC">PUBLIC</a></code> | *No description.* |
| <code><a href="#cdk-constructs.SubnetType.PRIVATE">PRIVATE</a></code> | *No description.* |

---

##### `PUBLIC` <a name="PUBLIC" id="cdk-constructs.SubnetType.PUBLIC"></a>

---


##### `PRIVATE` <a name="PRIVATE" id="cdk-constructs.SubnetType.PRIVATE"></a>

---

