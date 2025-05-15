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

<!-- TWINE PASSWORD  --><!-- aws codeartifact get-authorization-token --domain thron --domain-owner 499570923361 --query authorizationToken --output text -->
# API Reference <a name="API Reference" id="api-reference"></a>

## Constructs <a name="Constructs" id="Constructs"></a>

### DefaultValue <a name="DefaultValue" id="cdk-constructs.DefaultValue"></a>

#### Initializers <a name="Initializers" id="cdk-constructs.DefaultValue.Initializer"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

cdkconstructs.NewDefaultValue(scope Construct, id *string) DefaultValue
```

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.DefaultValue.Initializer.parameter.scope">scope</a></code> | <code>github.com/aws/constructs-go/constructs/v10.Construct</code> | *No description.* |
| <code><a href="#cdk-constructs.DefaultValue.Initializer.parameter.id">id</a></code> | <code>*string</code> | *No description.* |

---

##### `scope`<sup>Required</sup> <a name="scope" id="cdk-constructs.DefaultValue.Initializer.parameter.scope"></a>

- *Type:* github.com/aws/constructs-go/constructs/v10.Construct

---

##### `id`<sup>Required</sup> <a name="id" id="cdk-constructs.DefaultValue.Initializer.parameter.id"></a>

- *Type:* *string

---

#### Methods <a name="Methods" id="Methods"></a>

| **Name** | **Description** |
| --- | --- |
| <code><a href="#cdk-constructs.DefaultValue.toString">ToString</a></code> | Returns a string representation of this construct. |
| <code><a href="#cdk-constructs.DefaultValue.cdnDomainLong">CdnDomainLong</a></code> | *No description.* |
| <code><a href="#cdk-constructs.DefaultValue.privateRouteR53Zone">PrivateRouteR53Zone</a></code> | *No description.* |
| <code><a href="#cdk-constructs.DefaultValue.privateSubnetSelection">PrivateSubnetSelection</a></code> | *No description.* |
| <code><a href="#cdk-constructs.DefaultValue.sitename">Sitename</a></code> | *No description.* |
| <code><a href="#cdk-constructs.DefaultValue.vpc">Vpc</a></code> | *No description.* |
| <code><a href="#cdk-constructs.DefaultValue.vpcId">VpcId</a></code> | *No description.* |
| <code><a href="#cdk-constructs.DefaultValue.vpcIPV4Cidr">VpcIPV4Cidr</a></code> | *No description.* |
| <code><a href="#cdk-constructs.DefaultValue.vpcIPV6Cidr">VpcIPV6Cidr</a></code> | *No description.* |

---

##### `ToString` <a name="ToString" id="cdk-constructs.DefaultValue.toString"></a>

```go
func ToString() *string
```

Returns a string representation of this construct.

##### `CdnDomainLong` <a name="CdnDomainLong" id="cdk-constructs.DefaultValue.cdnDomainLong"></a>

```go
func CdnDomainLong() *string
```

##### `PrivateRouteR53Zone` <a name="PrivateRouteR53Zone" id="cdk-constructs.DefaultValue.privateRouteR53Zone"></a>

```go
func PrivateRouteR53Zone() IHostedZone
```

##### `PrivateSubnetSelection` <a name="PrivateSubnetSelection" id="cdk-constructs.DefaultValue.privateSubnetSelection"></a>

```go
func PrivateSubnetSelection() SubnetSelection
```

##### `Sitename` <a name="Sitename" id="cdk-constructs.DefaultValue.sitename"></a>

```go
func Sitename() *string
```

##### `Vpc` <a name="Vpc" id="cdk-constructs.DefaultValue.vpc"></a>

```go
func Vpc() IVpc
```

##### `VpcId` <a name="VpcId" id="cdk-constructs.DefaultValue.vpcId"></a>

```go
func VpcId() *string
```

##### `VpcIPV4Cidr` <a name="VpcIPV4Cidr" id="cdk-constructs.DefaultValue.vpcIPV4Cidr"></a>

```go
func VpcIPV4Cidr() *string
```

##### `VpcIPV6Cidr` <a name="VpcIPV6Cidr" id="cdk-constructs.DefaultValue.vpcIPV6Cidr"></a>

```go
func VpcIPV6Cidr() *string
```

#### Static Functions <a name="Static Functions" id="Static Functions"></a>

| **Name** | **Description** |
| --- | --- |
| <code><a href="#cdk-constructs.DefaultValue.isConstruct">IsConstruct</a></code> | Checks if `x` is a construct. |

---

##### `IsConstruct` <a name="IsConstruct" id="cdk-constructs.DefaultValue.isConstruct"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

cdkconstructs.DefaultValue_IsConstruct(x interface{}) *bool
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

- *Type:* interface{}

Any object.

---

#### Properties <a name="Properties" id="Properties"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.DefaultValue.property.node">Node</a></code> | <code>github.com/aws/constructs-go/constructs/v10.Node</code> | The tree node. |

---

##### `Node`<sup>Required</sup> <a name="Node" id="cdk-constructs.DefaultValue.property.node"></a>

```go
func Node() Node
```

- *Type:* github.com/aws/constructs-go/constructs/v10.Node

The tree node.

---


### DockerBuildAndPush <a name="DockerBuildAndPush" id="cdk-constructs.DockerBuildAndPush"></a>

#### Initializers <a name="Initializers" id="cdk-constructs.DockerBuildAndPush.Initializer"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

cdkconstructs.NewDockerBuildAndPush(scope Stack, id *string, directory *string, dockerfile *string) DockerBuildAndPush
```

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.DockerBuildAndPush.Initializer.parameter.scope">scope</a></code> | <code>github.com/aws/aws-cdk-go/awscdk/v2.Stack</code> | *No description.* |
| <code><a href="#cdk-constructs.DockerBuildAndPush.Initializer.parameter.id">id</a></code> | <code>*string</code> | *No description.* |
| <code><a href="#cdk-constructs.DockerBuildAndPush.Initializer.parameter.directory">directory</a></code> | <code>*string</code> | *No description.* |
| <code><a href="#cdk-constructs.DockerBuildAndPush.Initializer.parameter.dockerfile">dockerfile</a></code> | <code>*string</code> | *No description.* |

---

##### `scope`<sup>Required</sup> <a name="scope" id="cdk-constructs.DockerBuildAndPush.Initializer.parameter.scope"></a>

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.Stack

---

##### `id`<sup>Required</sup> <a name="id" id="cdk-constructs.DockerBuildAndPush.Initializer.parameter.id"></a>

- *Type:* *string

---

##### `directory`<sup>Required</sup> <a name="directory" id="cdk-constructs.DockerBuildAndPush.Initializer.parameter.directory"></a>

- *Type:* *string

---

##### `dockerfile`<sup>Optional</sup> <a name="dockerfile" id="cdk-constructs.DockerBuildAndPush.Initializer.parameter.dockerfile"></a>

- *Type:* *string

---

#### Methods <a name="Methods" id="Methods"></a>

| **Name** | **Description** |
| --- | --- |
| <code><a href="#cdk-constructs.DockerBuildAndPush.toString">ToString</a></code> | Returns a string representation of this construct. |
| <code><a href="#cdk-constructs.DockerBuildAndPush.addDependency">AddDependency</a></code> | Add a dependency between this stack and another stack. |
| <code><a href="#cdk-constructs.DockerBuildAndPush.addMetadata">AddMetadata</a></code> | Adds an arbitrary key-value pair, with information you want to record about the stack. |
| <code><a href="#cdk-constructs.DockerBuildAndPush.addTransform">AddTransform</a></code> | Add a Transform to this stack. A Transform is a macro that AWS CloudFormation uses to process your template. |
| <code><a href="#cdk-constructs.DockerBuildAndPush.exportStringListValue">ExportStringListValue</a></code> | Create a CloudFormation Export for a string list value. |
| <code><a href="#cdk-constructs.DockerBuildAndPush.exportValue">ExportValue</a></code> | Create a CloudFormation Export for a string value. |
| <code><a href="#cdk-constructs.DockerBuildAndPush.formatArn">FormatArn</a></code> | Creates an ARN from components. |
| <code><a href="#cdk-constructs.DockerBuildAndPush.getLogicalId">GetLogicalId</a></code> | Allocates a stack-unique CloudFormation-compatible logical identity for a specific resource. |
| <code><a href="#cdk-constructs.DockerBuildAndPush.regionalFact">RegionalFact</a></code> | Look up a fact value for the given fact for the region of this stack. |
| <code><a href="#cdk-constructs.DockerBuildAndPush.renameLogicalId">RenameLogicalId</a></code> | Rename a generated logical identities. |
| <code><a href="#cdk-constructs.DockerBuildAndPush.reportMissingContextKey">ReportMissingContextKey</a></code> | Indicate that a context key was expected. |
| <code><a href="#cdk-constructs.DockerBuildAndPush.resolve">Resolve</a></code> | Resolve a tokenized value in the context of the current stack. |
| <code><a href="#cdk-constructs.DockerBuildAndPush.splitArn">SplitArn</a></code> | Splits the provided ARN into its components. |
| <code><a href="#cdk-constructs.DockerBuildAndPush.toJsonString">ToJsonString</a></code> | Convert an object, potentially containing tokens, to a JSON string. |
| <code><a href="#cdk-constructs.DockerBuildAndPush.toYamlString">ToYamlString</a></code> | Convert an object, potentially containing tokens, to a YAML string. |

---

##### `ToString` <a name="ToString" id="cdk-constructs.DockerBuildAndPush.toString"></a>

```go
func ToString() *string
```

Returns a string representation of this construct.

##### `AddDependency` <a name="AddDependency" id="cdk-constructs.DockerBuildAndPush.addDependency"></a>

```go
func AddDependency(target Stack, reason *string)
```

Add a dependency between this stack and another stack.

This can be used to define dependencies between any two stacks within an
app, and also supports nested stacks.

###### `target`<sup>Required</sup> <a name="target" id="cdk-constructs.DockerBuildAndPush.addDependency.parameter.target"></a>

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.Stack

---

###### `reason`<sup>Optional</sup> <a name="reason" id="cdk-constructs.DockerBuildAndPush.addDependency.parameter.reason"></a>

- *Type:* *string

---

##### `AddMetadata` <a name="AddMetadata" id="cdk-constructs.DockerBuildAndPush.addMetadata"></a>

```go
func AddMetadata(key *string, value interface{})
```

Adds an arbitrary key-value pair, with information you want to record about the stack.

These get translated to the Metadata section of the generated template.

> [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/metadata-section-structure.html](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/metadata-section-structure.html)

###### `key`<sup>Required</sup> <a name="key" id="cdk-constructs.DockerBuildAndPush.addMetadata.parameter.key"></a>

- *Type:* *string

---

###### `value`<sup>Required</sup> <a name="value" id="cdk-constructs.DockerBuildAndPush.addMetadata.parameter.value"></a>

- *Type:* interface{}

---

##### `AddTransform` <a name="AddTransform" id="cdk-constructs.DockerBuildAndPush.addTransform"></a>

```go
func AddTransform(transform *string)
```

Add a Transform to this stack. A Transform is a macro that AWS CloudFormation uses to process your template.

Duplicate values are removed when stack is synthesized.

> [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/transform-section-structure.html](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/transform-section-structure.html)

*Example*

```go
declare const stack: Stack;

stack.addTransform('AWS::Serverless-2016-10-31')
```


###### `transform`<sup>Required</sup> <a name="transform" id="cdk-constructs.DockerBuildAndPush.addTransform.parameter.transform"></a>

- *Type:* *string

The transform to add.

---

##### `ExportStringListValue` <a name="ExportStringListValue" id="cdk-constructs.DockerBuildAndPush.exportStringListValue"></a>

```go
func ExportStringListValue(exportedValue interface{}, options ExportValueOptions) *[]*string
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

- *Type:* interface{}

---

###### `options`<sup>Optional</sup> <a name="options" id="cdk-constructs.DockerBuildAndPush.exportStringListValue.parameter.options"></a>

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.ExportValueOptions

---

##### `ExportValue` <a name="ExportValue" id="cdk-constructs.DockerBuildAndPush.exportValue"></a>

```go
func ExportValue(exportedValue interface{}, options ExportValueOptions) *string
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

- *Type:* interface{}

---

###### `options`<sup>Optional</sup> <a name="options" id="cdk-constructs.DockerBuildAndPush.exportValue.parameter.options"></a>

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.ExportValueOptions

---

##### `FormatArn` <a name="FormatArn" id="cdk-constructs.DockerBuildAndPush.formatArn"></a>

```go
func FormatArn(components ArnComponents) *string
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

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.ArnComponents

---

##### `GetLogicalId` <a name="GetLogicalId" id="cdk-constructs.DockerBuildAndPush.getLogicalId"></a>

```go
func GetLogicalId(element CfnElement) *string
```

Allocates a stack-unique CloudFormation-compatible logical identity for a specific resource.

This method is called when a `CfnElement` is created and used to render the
initial logical identity of resources. Logical ID renames are applied at
this stage.

This method uses the protected method `allocateLogicalId` to render the
logical ID for an element. To modify the naming scheme, extend the `Stack`
class and override this method.

###### `element`<sup>Required</sup> <a name="element" id="cdk-constructs.DockerBuildAndPush.getLogicalId.parameter.element"></a>

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.CfnElement

The CloudFormation element for which a logical identity is needed.

---

##### `RegionalFact` <a name="RegionalFact" id="cdk-constructs.DockerBuildAndPush.regionalFact"></a>

```go
func RegionalFact(factName *string, defaultValue *string) *string
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

- *Type:* *string

---

###### `defaultValue`<sup>Optional</sup> <a name="defaultValue" id="cdk-constructs.DockerBuildAndPush.regionalFact.parameter.defaultValue"></a>

- *Type:* *string

---

##### `RenameLogicalId` <a name="RenameLogicalId" id="cdk-constructs.DockerBuildAndPush.renameLogicalId"></a>

```go
func RenameLogicalId(oldId *string, newId *string)
```

Rename a generated logical identities.

To modify the naming scheme strategy, extend the `Stack` class and
override the `allocateLogicalId` method.

###### `oldId`<sup>Required</sup> <a name="oldId" id="cdk-constructs.DockerBuildAndPush.renameLogicalId.parameter.oldId"></a>

- *Type:* *string

---

###### `newId`<sup>Required</sup> <a name="newId" id="cdk-constructs.DockerBuildAndPush.renameLogicalId.parameter.newId"></a>

- *Type:* *string

---

##### `ReportMissingContextKey` <a name="ReportMissingContextKey" id="cdk-constructs.DockerBuildAndPush.reportMissingContextKey"></a>

```go
func ReportMissingContextKey(report MissingContext)
```

Indicate that a context key was expected.

Contains instructions which will be emitted into the cloud assembly on how
the key should be supplied.

###### `report`<sup>Required</sup> <a name="report" id="cdk-constructs.DockerBuildAndPush.reportMissingContextKey.parameter.report"></a>

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.cloud_assembly_schema.MissingContext

The set of parameters needed to obtain the context.

---

##### `Resolve` <a name="Resolve" id="cdk-constructs.DockerBuildAndPush.resolve"></a>

```go
func Resolve(obj interface{}) interface{}
```

Resolve a tokenized value in the context of the current stack.

###### `obj`<sup>Required</sup> <a name="obj" id="cdk-constructs.DockerBuildAndPush.resolve.parameter.obj"></a>

- *Type:* interface{}

---

##### `SplitArn` <a name="SplitArn" id="cdk-constructs.DockerBuildAndPush.splitArn"></a>

```go
func SplitArn(arn *string, arnFormat ArnFormat) ArnComponents
```

Splits the provided ARN into its components.

Works both if 'arn' is a string like 'arn:aws:s3:::bucket',
and a Token representing a dynamic CloudFormation expression
(in which case the returned components will also be dynamic CloudFormation expressions,
encoded as Tokens).

###### `arn`<sup>Required</sup> <a name="arn" id="cdk-constructs.DockerBuildAndPush.splitArn.parameter.arn"></a>

- *Type:* *string

the ARN to split into its components.

---

###### `arnFormat`<sup>Required</sup> <a name="arnFormat" id="cdk-constructs.DockerBuildAndPush.splitArn.parameter.arnFormat"></a>

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.ArnFormat

the expected format of 'arn' - depends on what format the service 'arn' represents uses.

---

##### `ToJsonString` <a name="ToJsonString" id="cdk-constructs.DockerBuildAndPush.toJsonString"></a>

```go
func ToJsonString(obj interface{}, space *f64) *string
```

Convert an object, potentially containing tokens, to a JSON string.

###### `obj`<sup>Required</sup> <a name="obj" id="cdk-constructs.DockerBuildAndPush.toJsonString.parameter.obj"></a>

- *Type:* interface{}

---

###### `space`<sup>Optional</sup> <a name="space" id="cdk-constructs.DockerBuildAndPush.toJsonString.parameter.space"></a>

- *Type:* *f64

---

##### `ToYamlString` <a name="ToYamlString" id="cdk-constructs.DockerBuildAndPush.toYamlString"></a>

```go
func ToYamlString(obj interface{}) *string
```

Convert an object, potentially containing tokens, to a YAML string.

###### `obj`<sup>Required</sup> <a name="obj" id="cdk-constructs.DockerBuildAndPush.toYamlString.parameter.obj"></a>

- *Type:* interface{}

---

#### Static Functions <a name="Static Functions" id="Static Functions"></a>

| **Name** | **Description** |
| --- | --- |
| <code><a href="#cdk-constructs.DockerBuildAndPush.isConstruct">IsConstruct</a></code> | Checks if `x` is a construct. |
| <code><a href="#cdk-constructs.DockerBuildAndPush.isStack">IsStack</a></code> | Return whether the given object is a Stack. |
| <code><a href="#cdk-constructs.DockerBuildAndPush.of">Of</a></code> | Looks up the first stack scope in which `construct` is defined. |

---

##### `IsConstruct` <a name="IsConstruct" id="cdk-constructs.DockerBuildAndPush.isConstruct"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

cdkconstructs.DockerBuildAndPush_IsConstruct(x interface{}) *bool
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

- *Type:* interface{}

Any object.

---

##### `IsStack` <a name="IsStack" id="cdk-constructs.DockerBuildAndPush.isStack"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

cdkconstructs.DockerBuildAndPush_IsStack(x interface{}) *bool
```

Return whether the given object is a Stack.

We do attribute detection since we can't reliably use 'instanceof'.

###### `x`<sup>Required</sup> <a name="x" id="cdk-constructs.DockerBuildAndPush.isStack.parameter.x"></a>

- *Type:* interface{}

---

##### `Of` <a name="Of" id="cdk-constructs.DockerBuildAndPush.of"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

cdkconstructs.DockerBuildAndPush_Of(construct IConstruct) Stack
```

Looks up the first stack scope in which `construct` is defined.

Fails if there is no stack up the tree.

###### `construct`<sup>Required</sup> <a name="construct" id="cdk-constructs.DockerBuildAndPush.of.parameter.construct"></a>

- *Type:* github.com/aws/constructs-go/constructs/v10.IConstruct

The construct to start the search from.

---

#### Properties <a name="Properties" id="Properties"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.DockerBuildAndPush.property.node">Node</a></code> | <code>github.com/aws/constructs-go/constructs/v10.Node</code> | The tree node. |
| <code><a href="#cdk-constructs.DockerBuildAndPush.property.account">Account</a></code> | <code>*string</code> | The AWS account into which this stack will be deployed. |
| <code><a href="#cdk-constructs.DockerBuildAndPush.property.artifactId">ArtifactId</a></code> | <code>*string</code> | The ID of the cloud assembly artifact for this stack. |
| <code><a href="#cdk-constructs.DockerBuildAndPush.property.availabilityZones">AvailabilityZones</a></code> | <code>*[]*string</code> | Returns the list of AZs that are available in the AWS environment (account/region) associated with this stack. |
| <code><a href="#cdk-constructs.DockerBuildAndPush.property.bundlingRequired">BundlingRequired</a></code> | <code>*bool</code> | Indicates whether the stack requires bundling or not. |
| <code><a href="#cdk-constructs.DockerBuildAndPush.property.dependencies">Dependencies</a></code> | <code>*[]github.com/aws/aws-cdk-go/awscdk/v2.Stack</code> | Return the stacks this stack depends on. |
| <code><a href="#cdk-constructs.DockerBuildAndPush.property.environment">Environment</a></code> | <code>*string</code> | The environment coordinates in which this stack is deployed. |
| <code><a href="#cdk-constructs.DockerBuildAndPush.property.nested">Nested</a></code> | <code>*bool</code> | Indicates if this is a nested stack, in which case `parentStack` will include a reference to it's parent. |
| <code><a href="#cdk-constructs.DockerBuildAndPush.property.notificationArns">NotificationArns</a></code> | <code>*[]*string</code> | Returns the list of notification Amazon Resource Names (ARNs) for the current stack. |
| <code><a href="#cdk-constructs.DockerBuildAndPush.property.partition">Partition</a></code> | <code>*string</code> | The partition in which this stack is defined. |
| <code><a href="#cdk-constructs.DockerBuildAndPush.property.region">Region</a></code> | <code>*string</code> | The AWS region into which this stack will be deployed (e.g. `us-west-2`). |
| <code><a href="#cdk-constructs.DockerBuildAndPush.property.stackId">StackId</a></code> | <code>*string</code> | The ID of the stack. |
| <code><a href="#cdk-constructs.DockerBuildAndPush.property.stackName">StackName</a></code> | <code>*string</code> | The concrete CloudFormation physical stack name. |
| <code><a href="#cdk-constructs.DockerBuildAndPush.property.synthesizer">Synthesizer</a></code> | <code>github.com/aws/aws-cdk-go/awscdk/v2.IStackSynthesizer</code> | Synthesis method for this stack. |
| <code><a href="#cdk-constructs.DockerBuildAndPush.property.tags">Tags</a></code> | <code>github.com/aws/aws-cdk-go/awscdk/v2.TagManager</code> | Tags to be applied to the stack. |
| <code><a href="#cdk-constructs.DockerBuildAndPush.property.templateFile">TemplateFile</a></code> | <code>*string</code> | The name of the CloudFormation template file emitted to the output directory during synthesis. |
| <code><a href="#cdk-constructs.DockerBuildAndPush.property.templateOptions">TemplateOptions</a></code> | <code>github.com/aws/aws-cdk-go/awscdk/v2.ITemplateOptions</code> | Options for CloudFormation template (like version, transform, description). |
| <code><a href="#cdk-constructs.DockerBuildAndPush.property.urlSuffix">UrlSuffix</a></code> | <code>*string</code> | The Amazon domain suffix for the region in which this stack is defined. |
| <code><a href="#cdk-constructs.DockerBuildAndPush.property.nestedStackParent">NestedStackParent</a></code> | <code>github.com/aws/aws-cdk-go/awscdk/v2.Stack</code> | If this is a nested stack, returns it's parent stack. |
| <code><a href="#cdk-constructs.DockerBuildAndPush.property.nestedStackResource">NestedStackResource</a></code> | <code>github.com/aws/aws-cdk-go/awscdk/v2.CfnResource</code> | If this is a nested stack, this represents its `AWS::CloudFormation::Stack` resource. |
| <code><a href="#cdk-constructs.DockerBuildAndPush.property.terminationProtection">TerminationProtection</a></code> | <code>*bool</code> | Whether termination protection is enabled for this stack. |
| <code><a href="#cdk-constructs.DockerBuildAndPush.property.ecrImage">EcrImage</a></code> | <code>github.com/aws/aws-cdk-go/awscdk/v2.aws_ecs.EcrImage</code> | *No description.* |
| <code><a href="#cdk-constructs.DockerBuildAndPush.property.lambdaDockerImageCode">LambdaDockerImageCode</a></code> | <code>github.com/aws/aws-cdk-go/awscdk/v2.aws_lambda.DockerImageCode</code> | *No description.* |

---

##### `Node`<sup>Required</sup> <a name="Node" id="cdk-constructs.DockerBuildAndPush.property.node"></a>

```go
func Node() Node
```

- *Type:* github.com/aws/constructs-go/constructs/v10.Node

The tree node.

---

##### `Account`<sup>Required</sup> <a name="Account" id="cdk-constructs.DockerBuildAndPush.property.account"></a>

```go
func Account() *string
```

- *Type:* *string

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

##### `ArtifactId`<sup>Required</sup> <a name="ArtifactId" id="cdk-constructs.DockerBuildAndPush.property.artifactId"></a>

```go
func ArtifactId() *string
```

- *Type:* *string

The ID of the cloud assembly artifact for this stack.

---

##### `AvailabilityZones`<sup>Required</sup> <a name="AvailabilityZones" id="cdk-constructs.DockerBuildAndPush.property.availabilityZones"></a>

```go
func AvailabilityZones() *[]*string
```

- *Type:* *[]*string

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

##### `BundlingRequired`<sup>Required</sup> <a name="BundlingRequired" id="cdk-constructs.DockerBuildAndPush.property.bundlingRequired"></a>

```go
func BundlingRequired() *bool
```

- *Type:* *bool

Indicates whether the stack requires bundling or not.

---

##### `Dependencies`<sup>Required</sup> <a name="Dependencies" id="cdk-constructs.DockerBuildAndPush.property.dependencies"></a>

```go
func Dependencies() *[]Stack
```

- *Type:* *[]github.com/aws/aws-cdk-go/awscdk/v2.Stack

Return the stacks this stack depends on.

---

##### `Environment`<sup>Required</sup> <a name="Environment" id="cdk-constructs.DockerBuildAndPush.property.environment"></a>

```go
func Environment() *string
```

- *Type:* *string

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

##### `Nested`<sup>Required</sup> <a name="Nested" id="cdk-constructs.DockerBuildAndPush.property.nested"></a>

```go
func Nested() *bool
```

- *Type:* *bool

Indicates if this is a nested stack, in which case `parentStack` will include a reference to it's parent.

---

##### `NotificationArns`<sup>Required</sup> <a name="NotificationArns" id="cdk-constructs.DockerBuildAndPush.property.notificationArns"></a>

```go
func NotificationArns() *[]*string
```

- *Type:* *[]*string

Returns the list of notification Amazon Resource Names (ARNs) for the current stack.

---

##### `Partition`<sup>Required</sup> <a name="Partition" id="cdk-constructs.DockerBuildAndPush.property.partition"></a>

```go
func Partition() *string
```

- *Type:* *string

The partition in which this stack is defined.

---

##### `Region`<sup>Required</sup> <a name="Region" id="cdk-constructs.DockerBuildAndPush.property.region"></a>

```go
func Region() *string
```

- *Type:* *string

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

##### `StackId`<sup>Required</sup> <a name="StackId" id="cdk-constructs.DockerBuildAndPush.property.stackId"></a>

```go
func StackId() *string
```

- *Type:* *string

The ID of the stack.

---

*Example*

```go
// After resolving, looks like
'arn:aws:cloudformation:us-west-2:123456789012:stack/teststack/51af3dc0-da77-11e4-872e-1234567db123'
```


##### `StackName`<sup>Required</sup> <a name="StackName" id="cdk-constructs.DockerBuildAndPush.property.stackName"></a>

```go
func StackName() *string
```

- *Type:* *string

The concrete CloudFormation physical stack name.

This is either the name defined explicitly in the `stackName` prop or
allocated based on the stack's location in the construct tree. Stacks that
are directly defined under the app use their construct `id` as their stack
name. Stacks that are defined deeper within the tree will use a hashed naming
scheme based on the construct path to ensure uniqueness.

If you wish to obtain the deploy-time AWS::StackName intrinsic,
you can use `Aws.STACK_NAME` directly.

---

##### `Synthesizer`<sup>Required</sup> <a name="Synthesizer" id="cdk-constructs.DockerBuildAndPush.property.synthesizer"></a>

```go
func Synthesizer() IStackSynthesizer
```

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.IStackSynthesizer

Synthesis method for this stack.

---

##### `Tags`<sup>Required</sup> <a name="Tags" id="cdk-constructs.DockerBuildAndPush.property.tags"></a>

```go
func Tags() TagManager
```

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.TagManager

Tags to be applied to the stack.

---

##### `TemplateFile`<sup>Required</sup> <a name="TemplateFile" id="cdk-constructs.DockerBuildAndPush.property.templateFile"></a>

```go
func TemplateFile() *string
```

- *Type:* *string

The name of the CloudFormation template file emitted to the output directory during synthesis.

Example value: `MyStack.template.json`

---

##### `TemplateOptions`<sup>Required</sup> <a name="TemplateOptions" id="cdk-constructs.DockerBuildAndPush.property.templateOptions"></a>

```go
func TemplateOptions() ITemplateOptions
```

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.ITemplateOptions

Options for CloudFormation template (like version, transform, description).

---

##### `UrlSuffix`<sup>Required</sup> <a name="UrlSuffix" id="cdk-constructs.DockerBuildAndPush.property.urlSuffix"></a>

```go
func UrlSuffix() *string
```

- *Type:* *string

The Amazon domain suffix for the region in which this stack is defined.

---

##### `NestedStackParent`<sup>Optional</sup> <a name="NestedStackParent" id="cdk-constructs.DockerBuildAndPush.property.nestedStackParent"></a>

```go
func NestedStackParent() Stack
```

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.Stack

If this is a nested stack, returns it's parent stack.

---

##### `NestedStackResource`<sup>Optional</sup> <a name="NestedStackResource" id="cdk-constructs.DockerBuildAndPush.property.nestedStackResource"></a>

```go
func NestedStackResource() CfnResource
```

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.CfnResource

If this is a nested stack, this represents its `AWS::CloudFormation::Stack` resource.

`undefined` for top-level (non-nested) stacks.

---

##### `TerminationProtection`<sup>Required</sup> <a name="TerminationProtection" id="cdk-constructs.DockerBuildAndPush.property.terminationProtection"></a>

```go
func TerminationProtection() *bool
```

- *Type:* *bool

Whether termination protection is enabled for this stack.

---

##### `EcrImage`<sup>Required</sup> <a name="EcrImage" id="cdk-constructs.DockerBuildAndPush.property.ecrImage"></a>

```go
func EcrImage() EcrImage
```

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_ecs.EcrImage

---

##### `LambdaDockerImageCode`<sup>Required</sup> <a name="LambdaDockerImageCode" id="cdk-constructs.DockerBuildAndPush.property.lambdaDockerImageCode"></a>

```go
func LambdaDockerImageCode() DockerImageCode
```

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_lambda.DockerImageCode

---


### ECRDeployment <a name="ECRDeployment" id="cdk-constructs.ECRDeployment"></a>

#### Initializers <a name="Initializers" id="cdk-constructs.ECRDeployment.Initializer"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

cdkconstructs.NewECRDeployment(scope Construct, id *string, props ECRDeploymentProps) ECRDeployment
```

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.ECRDeployment.Initializer.parameter.scope">scope</a></code> | <code>github.com/aws/constructs-go/constructs/v10.Construct</code> | *No description.* |
| <code><a href="#cdk-constructs.ECRDeployment.Initializer.parameter.id">id</a></code> | <code>*string</code> | *No description.* |
| <code><a href="#cdk-constructs.ECRDeployment.Initializer.parameter.props">props</a></code> | <code><a href="#cdk-constructs.ECRDeploymentProps">ECRDeploymentProps</a></code> | *No description.* |

---

##### `scope`<sup>Required</sup> <a name="scope" id="cdk-constructs.ECRDeployment.Initializer.parameter.scope"></a>

- *Type:* github.com/aws/constructs-go/constructs/v10.Construct

---

##### `id`<sup>Required</sup> <a name="id" id="cdk-constructs.ECRDeployment.Initializer.parameter.id"></a>

- *Type:* *string

---

##### `props`<sup>Required</sup> <a name="props" id="cdk-constructs.ECRDeployment.Initializer.parameter.props"></a>

- *Type:* <a href="#cdk-constructs.ECRDeploymentProps">ECRDeploymentProps</a>

---

#### Methods <a name="Methods" id="Methods"></a>

| **Name** | **Description** |
| --- | --- |
| <code><a href="#cdk-constructs.ECRDeployment.toString">ToString</a></code> | Returns a string representation of this construct. |
| <code><a href="#cdk-constructs.ECRDeployment.addToPrincipalPolicy">AddToPrincipalPolicy</a></code> | *No description.* |

---

##### `ToString` <a name="ToString" id="cdk-constructs.ECRDeployment.toString"></a>

```go
func ToString() *string
```

Returns a string representation of this construct.

##### `AddToPrincipalPolicy` <a name="AddToPrincipalPolicy" id="cdk-constructs.ECRDeployment.addToPrincipalPolicy"></a>

```go
func AddToPrincipalPolicy(statement PolicyStatement) AddToPrincipalPolicyResult
```

###### `statement`<sup>Required</sup> <a name="statement" id="cdk-constructs.ECRDeployment.addToPrincipalPolicy.parameter.statement"></a>

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_iam.PolicyStatement

---

#### Static Functions <a name="Static Functions" id="Static Functions"></a>

| **Name** | **Description** |
| --- | --- |
| <code><a href="#cdk-constructs.ECRDeployment.isConstruct">IsConstruct</a></code> | Checks if `x` is a construct. |

---

##### `IsConstruct` <a name="IsConstruct" id="cdk-constructs.ECRDeployment.isConstruct"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

cdkconstructs.ECRDeployment_IsConstruct(x interface{}) *bool
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

- *Type:* interface{}

Any object.

---

#### Properties <a name="Properties" id="Properties"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.ECRDeployment.property.node">Node</a></code> | <code>github.com/aws/constructs-go/constructs/v10.Node</code> | The tree node. |

---

##### `Node`<sup>Required</sup> <a name="Node" id="cdk-constructs.ECRDeployment.property.node"></a>

```go
func Node() Node
```

- *Type:* github.com/aws/constructs-go/constructs/v10.Node

The tree node.

---


### EndpointAlb <a name="EndpointAlb" id="cdk-constructs.EndpointAlb"></a>

#### Methods <a name="Methods" id="Methods"></a>

| **Name** | **Description** |
| --- | --- |
| <code><a href="#cdk-constructs.EndpointAlb.toString">ToString</a></code> | Returns a string representation of this construct. |
| <code><a href="#cdk-constructs.EndpointAlb.buildTGConditions">BuildTGConditions</a></code> | Build ALB Listener routing condition based on routing token and service name. |
| <code><a href="#cdk-constructs.EndpointAlb.withTarget">WithTarget</a></code> | Set the target of the endpoint. |

---

##### `ToString` <a name="ToString" id="cdk-constructs.EndpointAlb.toString"></a>

```go
func ToString() *string
```

Returns a string representation of this construct.

##### `BuildTGConditions` <a name="BuildTGConditions" id="cdk-constructs.EndpointAlb.buildTGConditions"></a>

```go
func BuildTGConditions(serviceName *string, routingTokenPrefix *string, serviceGroup *string) *[]ListenerCondition
```

Build ALB Listener routing condition based on routing token and service name.

###### `serviceName`<sup>Required</sup> <a name="serviceName" id="cdk-constructs.EndpointAlb.buildTGConditions.parameter.serviceName"></a>

- *Type:* *string

service name.

---

###### `routingTokenPrefix`<sup>Required</sup> <a name="routingTokenPrefix" id="cdk-constructs.EndpointAlb.buildTGConditions.parameter.routingTokenPrefix"></a>

- *Type:* *string

routing token.

---

###### `serviceGroup`<sup>Required</sup> <a name="serviceGroup" id="cdk-constructs.EndpointAlb.buildTGConditions.parameter.serviceGroup"></a>

- *Type:* *string

---

##### `WithTarget` <a name="WithTarget" id="cdk-constructs.EndpointAlb.withTarget"></a>

```go
func WithTarget(targetGroup ApplicationTargetGroup) EndpointAlb
```

Set the target of the endpoint.

###### `targetGroup`<sup>Required</sup> <a name="targetGroup" id="cdk-constructs.EndpointAlb.withTarget.parameter.targetGroup"></a>

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_elasticloadbalancingv2.ApplicationTargetGroup

---

#### Static Functions <a name="Static Functions" id="Static Functions"></a>

| **Name** | **Description** |
| --- | --- |
| <code><a href="#cdk-constructs.EndpointAlb.isConstruct">IsConstruct</a></code> | Checks if `x` is a construct. |
| <code><a href="#cdk-constructs.EndpointAlb.legacyEndpoint">LegacyEndpoint</a></code> | Build an endpoint without any validation on path prefix. |
| <code><a href="#cdk-constructs.EndpointAlb.thronEndpoint">ThronEndpoint</a></code> | Build an endpoint using thron's conventions on path prefix. |

---

##### `IsConstruct` <a name="IsConstruct" id="cdk-constructs.EndpointAlb.isConstruct"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

cdkconstructs.EndpointAlb_IsConstruct(x interface{}) *bool
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

- *Type:* interface{}

Any object.

---

##### `LegacyEndpoint` <a name="LegacyEndpoint" id="cdk-constructs.EndpointAlb.legacyEndpoint"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

cdkconstructs.EndpointAlb_LegacyEndpoint(scope Construct, id *string, props LegacyEndpointAlbProps) EndpointAlb
```

Build an endpoint without any validation on path prefix.

###### `scope`<sup>Required</sup> <a name="scope" id="cdk-constructs.EndpointAlb.legacyEndpoint.parameter.scope"></a>

- *Type:* github.com/aws/constructs-go/constructs/v10.Construct

---

###### `id`<sup>Required</sup> <a name="id" id="cdk-constructs.EndpointAlb.legacyEndpoint.parameter.id"></a>

- *Type:* *string

---

###### `props`<sup>Required</sup> <a name="props" id="cdk-constructs.EndpointAlb.legacyEndpoint.parameter.props"></a>

- *Type:* <a href="#cdk-constructs.LegacyEndpointAlbProps">LegacyEndpointAlbProps</a>

---

##### `ThronEndpoint` <a name="ThronEndpoint" id="cdk-constructs.EndpointAlb.thronEndpoint"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

cdkconstructs.EndpointAlb_ThronEndpoint(scope Construct, id *string, props ThronEndpointAlbProps) EndpointAlb
```

Build an endpoint using thron's conventions on path prefix.

###### `scope`<sup>Required</sup> <a name="scope" id="cdk-constructs.EndpointAlb.thronEndpoint.parameter.scope"></a>

- *Type:* github.com/aws/constructs-go/constructs/v10.Construct

---

###### `id`<sup>Required</sup> <a name="id" id="cdk-constructs.EndpointAlb.thronEndpoint.parameter.id"></a>

- *Type:* *string

---

###### `props`<sup>Required</sup> <a name="props" id="cdk-constructs.EndpointAlb.thronEndpoint.parameter.props"></a>

- *Type:* <a href="#cdk-constructs.ThronEndpointAlbProps">ThronEndpointAlbProps</a>

---

#### Properties <a name="Properties" id="Properties"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.EndpointAlb.property.node">Node</a></code> | <code>github.com/aws/constructs-go/constructs/v10.Node</code> | The tree node. |
| <code><a href="#cdk-constructs.EndpointAlb.property.defaultValue">DefaultValue</a></code> | <code><a href="#cdk-constructs.DefaultValue">DefaultValue</a></code> | Default Vaule class. |
| <code><a href="#cdk-constructs.EndpointAlb.property.routingTokenPrefix">RoutingTokenPrefix</a></code> | <code>*string</code> | Routing path, validated against selected `serviceGroup` conventions. |
| <code><a href="#cdk-constructs.EndpointAlb.property.serviceGroup">ServiceGroup</a></code> | <code><a href="#cdk-constructs.ServiceGroup">ServiceGroup</a></code> | Service group. |
| <code><a href="#cdk-constructs.EndpointAlb.property.sitename">Sitename</a></code> | <code>*string</code> | Sitename where the construct is being deployed. |
| <code><a href="#cdk-constructs.EndpointAlb.property.listener">Listener</a></code> | <code>github.com/aws/aws-cdk-go/awscdk/v2.aws_elasticloadbalancingv2.IApplicationListener</code> | ALB Listener where the endpoint is attached. |
| <code><a href="#cdk-constructs.EndpointAlb.property.rulePriority">RulePriority</a></code> | <code>github.com/aws/aws-cdk-go/awscdk/v2.Reference</code> | ALB Listener Rule priority used for this endpoint. |
| <code><a href="#cdk-constructs.EndpointAlb.property.serviceName">ServiceName</a></code> | <code>*string</code> | Name of the service (generated). |
| <code><a href="#cdk-constructs.EndpointAlb.property.stack">Stack</a></code> | <code>github.com/aws/aws-cdk-go/awscdk/v2.Stack</code> | The reference of parent Stack. |
| <code><a href="#cdk-constructs.EndpointAlb.property.version">Version</a></code> | <code>*f64</code> | Version of the endpoint (available only on thronEndpoints). |
| <code><a href="#cdk-constructs.EndpointAlb.property.visibility">Visibility</a></code> | <code><a href="#cdk-constructs.EndpointVisibility">EndpointVisibility</a></code> | Visibility of the endpint (available only on thronEndpoints). |

---

##### `Node`<sup>Required</sup> <a name="Node" id="cdk-constructs.EndpointAlb.property.node"></a>

```go
func Node() Node
```

- *Type:* github.com/aws/constructs-go/constructs/v10.Node

The tree node.

---

##### `DefaultValue`<sup>Required</sup> <a name="DefaultValue" id="cdk-constructs.EndpointAlb.property.defaultValue"></a>

```go
func DefaultValue() DefaultValue
```

- *Type:* <a href="#cdk-constructs.DefaultValue">DefaultValue</a>

Default Vaule class.

---

##### `RoutingTokenPrefix`<sup>Required</sup> <a name="RoutingTokenPrefix" id="cdk-constructs.EndpointAlb.property.routingTokenPrefix"></a>

```go
func RoutingTokenPrefix() *string
```

- *Type:* *string

Routing path, validated against selected `serviceGroup` conventions.

---

##### `ServiceGroup`<sup>Required</sup> <a name="ServiceGroup" id="cdk-constructs.EndpointAlb.property.serviceGroup"></a>

```go
func ServiceGroup() ServiceGroup
```

- *Type:* <a href="#cdk-constructs.ServiceGroup">ServiceGroup</a>

Service group.

---

##### `Sitename`<sup>Required</sup> <a name="Sitename" id="cdk-constructs.EndpointAlb.property.sitename"></a>

```go
func Sitename() *string
```

- *Type:* *string

Sitename where the construct is being deployed.

---

##### `Listener`<sup>Optional</sup> <a name="Listener" id="cdk-constructs.EndpointAlb.property.listener"></a>

```go
func Listener() IApplicationListener
```

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_elasticloadbalancingv2.IApplicationListener

ALB Listener where the endpoint is attached.

---

##### `RulePriority`<sup>Optional</sup> <a name="RulePriority" id="cdk-constructs.EndpointAlb.property.rulePriority"></a>

```go
func RulePriority() Reference
```

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.Reference

ALB Listener Rule priority used for this endpoint.

---

##### `ServiceName`<sup>Optional</sup> <a name="ServiceName" id="cdk-constructs.EndpointAlb.property.serviceName"></a>

```go
func ServiceName() *string
```

- *Type:* *string

Name of the service (generated).

---

##### `Stack`<sup>Optional</sup> <a name="Stack" id="cdk-constructs.EndpointAlb.property.stack"></a>

```go
func Stack() Stack
```

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.Stack

The reference of parent Stack.

---

##### `Version`<sup>Optional</sup> <a name="Version" id="cdk-constructs.EndpointAlb.property.version"></a>

```go
func Version() *f64
```

- *Type:* *f64

Version of the endpoint (available only on thronEndpoints).

---

##### `Visibility`<sup>Optional</sup> <a name="Visibility" id="cdk-constructs.EndpointAlb.property.visibility"></a>

```go
func Visibility() EndpointVisibility
```

- *Type:* <a href="#cdk-constructs.EndpointVisibility">EndpointVisibility</a>

Visibility of the endpint (available only on thronEndpoints).

---


### SsmParameterReader <a name="SsmParameterReader" id="cdk-constructs.SsmParameterReader"></a>

Class instantiating the SSMParameterReader custom resources, which allows you to read encrypted ssm parameters and use them as input for other constructs, i.e. lambda environment.

*Example*

```go
// Example automatically generated from non-compiling source. May contain errors.
ssmParameterValue := NewSsmParameterReader(this, jsii.String("example-id"), map[string]*string{
	"parameterName": jsii.String("/example/param"),
}).stringValue
```


#### Initializers <a name="Initializers" id="cdk-constructs.SsmParameterReader.Initializer"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

cdkconstructs.NewSsmParameterReader(scope Construct, id *string, props SsmParameterReaderProps) SsmParameterReader
```

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.SsmParameterReader.Initializer.parameter.scope">scope</a></code> | <code>github.com/aws/constructs-go/constructs/v10.Construct</code> | *No description.* |
| <code><a href="#cdk-constructs.SsmParameterReader.Initializer.parameter.id">id</a></code> | <code>*string</code> | *No description.* |
| <code><a href="#cdk-constructs.SsmParameterReader.Initializer.parameter.props">props</a></code> | <code><a href="#cdk-constructs.SsmParameterReaderProps">SsmParameterReaderProps</a></code> | *No description.* |

---

##### `scope`<sup>Required</sup> <a name="scope" id="cdk-constructs.SsmParameterReader.Initializer.parameter.scope"></a>

- *Type:* github.com/aws/constructs-go/constructs/v10.Construct

---

##### `id`<sup>Required</sup> <a name="id" id="cdk-constructs.SsmParameterReader.Initializer.parameter.id"></a>

- *Type:* *string

---

##### `props`<sup>Required</sup> <a name="props" id="cdk-constructs.SsmParameterReader.Initializer.parameter.props"></a>

- *Type:* <a href="#cdk-constructs.SsmParameterReaderProps">SsmParameterReaderProps</a>

---

#### Methods <a name="Methods" id="Methods"></a>

| **Name** | **Description** |
| --- | --- |
| <code><a href="#cdk-constructs.SsmParameterReader.toString">ToString</a></code> | Returns a string representation of this construct. |

---

##### `ToString` <a name="ToString" id="cdk-constructs.SsmParameterReader.toString"></a>

```go
func ToString() *string
```

Returns a string representation of this construct.

#### Static Functions <a name="Static Functions" id="Static Functions"></a>

| **Name** | **Description** |
| --- | --- |
| <code><a href="#cdk-constructs.SsmParameterReader.isConstruct">IsConstruct</a></code> | Checks if `x` is a construct. |

---

##### `IsConstruct` <a name="IsConstruct" id="cdk-constructs.SsmParameterReader.isConstruct"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

cdkconstructs.SsmParameterReader_IsConstruct(x interface{}) *bool
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

- *Type:* interface{}

Any object.

---

#### Properties <a name="Properties" id="Properties"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.SsmParameterReader.property.node">Node</a></code> | <code>github.com/aws/constructs-go/constructs/v10.Node</code> | The tree node. |
| <code><a href="#cdk-constructs.SsmParameterReader.property.stringValue">StringValue</a></code> | <code>*string</code> | Unencrypted Value of the SSM Parameter. |

---

##### `Node`<sup>Required</sup> <a name="Node" id="cdk-constructs.SsmParameterReader.property.node"></a>

```go
func Node() Node
```

- *Type:* github.com/aws/constructs-go/constructs/v10.Node

The tree node.

---

##### `StringValue`<sup>Required</sup> <a name="StringValue" id="cdk-constructs.SsmParameterReader.property.stringValue"></a>

```go
func StringValue() *string
```

- *Type:* *string

Unencrypted Value of the SSM Parameter.

---


### ThronAcmCertificate <a name="ThronAcmCertificate" id="cdk-constructs.ThronAcmCertificate"></a>

#### Initializers <a name="Initializers" id="cdk-constructs.ThronAcmCertificate.Initializer"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

cdkconstructs.NewThronAcmCertificate(scope Stack, id *string, props ThronAcmCertificateProps) ThronAcmCertificate
```

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.ThronAcmCertificate.Initializer.parameter.scope">scope</a></code> | <code>github.com/aws/aws-cdk-go/awscdk/v2.Stack</code> | *No description.* |
| <code><a href="#cdk-constructs.ThronAcmCertificate.Initializer.parameter.id">id</a></code> | <code>*string</code> | *No description.* |
| <code><a href="#cdk-constructs.ThronAcmCertificate.Initializer.parameter.props">props</a></code> | <code><a href="#cdk-constructs.ThronAcmCertificateProps">ThronAcmCertificateProps</a></code> | *No description.* |

---

##### `scope`<sup>Required</sup> <a name="scope" id="cdk-constructs.ThronAcmCertificate.Initializer.parameter.scope"></a>

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.Stack

---

##### `id`<sup>Required</sup> <a name="id" id="cdk-constructs.ThronAcmCertificate.Initializer.parameter.id"></a>

- *Type:* *string

---

##### `props`<sup>Required</sup> <a name="props" id="cdk-constructs.ThronAcmCertificate.Initializer.parameter.props"></a>

- *Type:* <a href="#cdk-constructs.ThronAcmCertificateProps">ThronAcmCertificateProps</a>

---

#### Methods <a name="Methods" id="Methods"></a>

| **Name** | **Description** |
| --- | --- |
| <code><a href="#cdk-constructs.ThronAcmCertificate.toString">ToString</a></code> | Returns a string representation of this construct. |
| <code><a href="#cdk-constructs.ThronAcmCertificate.addDependency">AddDependency</a></code> | Add a dependency between this stack and another stack. |
| <code><a href="#cdk-constructs.ThronAcmCertificate.addMetadata">AddMetadata</a></code> | Adds an arbitrary key-value pair, with information you want to record about the stack. |
| <code><a href="#cdk-constructs.ThronAcmCertificate.addTransform">AddTransform</a></code> | Add a Transform to this stack. A Transform is a macro that AWS CloudFormation uses to process your template. |
| <code><a href="#cdk-constructs.ThronAcmCertificate.exportStringListValue">ExportStringListValue</a></code> | Create a CloudFormation Export for a string list value. |
| <code><a href="#cdk-constructs.ThronAcmCertificate.exportValue">ExportValue</a></code> | Create a CloudFormation Export for a string value. |
| <code><a href="#cdk-constructs.ThronAcmCertificate.formatArn">FormatArn</a></code> | Creates an ARN from components. |
| <code><a href="#cdk-constructs.ThronAcmCertificate.getLogicalId">GetLogicalId</a></code> | Allocates a stack-unique CloudFormation-compatible logical identity for a specific resource. |
| <code><a href="#cdk-constructs.ThronAcmCertificate.regionalFact">RegionalFact</a></code> | Look up a fact value for the given fact for the region of this stack. |
| <code><a href="#cdk-constructs.ThronAcmCertificate.renameLogicalId">RenameLogicalId</a></code> | Rename a generated logical identities. |
| <code><a href="#cdk-constructs.ThronAcmCertificate.reportMissingContextKey">ReportMissingContextKey</a></code> | Indicate that a context key was expected. |
| <code><a href="#cdk-constructs.ThronAcmCertificate.resolve">Resolve</a></code> | Resolve a tokenized value in the context of the current stack. |
| <code><a href="#cdk-constructs.ThronAcmCertificate.splitArn">SplitArn</a></code> | Splits the provided ARN into its components. |
| <code><a href="#cdk-constructs.ThronAcmCertificate.toJsonString">ToJsonString</a></code> | Convert an object, potentially containing tokens, to a JSON string. |
| <code><a href="#cdk-constructs.ThronAcmCertificate.toYamlString">ToYamlString</a></code> | Convert an object, potentially containing tokens, to a YAML string. |

---

##### `ToString` <a name="ToString" id="cdk-constructs.ThronAcmCertificate.toString"></a>

```go
func ToString() *string
```

Returns a string representation of this construct.

##### `AddDependency` <a name="AddDependency" id="cdk-constructs.ThronAcmCertificate.addDependency"></a>

```go
func AddDependency(target Stack, reason *string)
```

Add a dependency between this stack and another stack.

This can be used to define dependencies between any two stacks within an
app, and also supports nested stacks.

###### `target`<sup>Required</sup> <a name="target" id="cdk-constructs.ThronAcmCertificate.addDependency.parameter.target"></a>

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.Stack

---

###### `reason`<sup>Optional</sup> <a name="reason" id="cdk-constructs.ThronAcmCertificate.addDependency.parameter.reason"></a>

- *Type:* *string

---

##### `AddMetadata` <a name="AddMetadata" id="cdk-constructs.ThronAcmCertificate.addMetadata"></a>

```go
func AddMetadata(key *string, value interface{})
```

Adds an arbitrary key-value pair, with information you want to record about the stack.

These get translated to the Metadata section of the generated template.

> [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/metadata-section-structure.html](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/metadata-section-structure.html)

###### `key`<sup>Required</sup> <a name="key" id="cdk-constructs.ThronAcmCertificate.addMetadata.parameter.key"></a>

- *Type:* *string

---

###### `value`<sup>Required</sup> <a name="value" id="cdk-constructs.ThronAcmCertificate.addMetadata.parameter.value"></a>

- *Type:* interface{}

---

##### `AddTransform` <a name="AddTransform" id="cdk-constructs.ThronAcmCertificate.addTransform"></a>

```go
func AddTransform(transform *string)
```

Add a Transform to this stack. A Transform is a macro that AWS CloudFormation uses to process your template.

Duplicate values are removed when stack is synthesized.

> [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/transform-section-structure.html](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/transform-section-structure.html)

*Example*

```go
declare const stack: Stack;

stack.addTransform('AWS::Serverless-2016-10-31')
```


###### `transform`<sup>Required</sup> <a name="transform" id="cdk-constructs.ThronAcmCertificate.addTransform.parameter.transform"></a>

- *Type:* *string

The transform to add.

---

##### `ExportStringListValue` <a name="ExportStringListValue" id="cdk-constructs.ThronAcmCertificate.exportStringListValue"></a>

```go
func ExportStringListValue(exportedValue interface{}, options ExportValueOptions) *[]*string
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

- *Type:* interface{}

---

###### `options`<sup>Optional</sup> <a name="options" id="cdk-constructs.ThronAcmCertificate.exportStringListValue.parameter.options"></a>

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.ExportValueOptions

---

##### `ExportValue` <a name="ExportValue" id="cdk-constructs.ThronAcmCertificate.exportValue"></a>

```go
func ExportValue(exportedValue interface{}, options ExportValueOptions) *string
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

- *Type:* interface{}

---

###### `options`<sup>Optional</sup> <a name="options" id="cdk-constructs.ThronAcmCertificate.exportValue.parameter.options"></a>

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.ExportValueOptions

---

##### `FormatArn` <a name="FormatArn" id="cdk-constructs.ThronAcmCertificate.formatArn"></a>

```go
func FormatArn(components ArnComponents) *string
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

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.ArnComponents

---

##### `GetLogicalId` <a name="GetLogicalId" id="cdk-constructs.ThronAcmCertificate.getLogicalId"></a>

```go
func GetLogicalId(element CfnElement) *string
```

Allocates a stack-unique CloudFormation-compatible logical identity for a specific resource.

This method is called when a `CfnElement` is created and used to render the
initial logical identity of resources. Logical ID renames are applied at
this stage.

This method uses the protected method `allocateLogicalId` to render the
logical ID for an element. To modify the naming scheme, extend the `Stack`
class and override this method.

###### `element`<sup>Required</sup> <a name="element" id="cdk-constructs.ThronAcmCertificate.getLogicalId.parameter.element"></a>

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.CfnElement

The CloudFormation element for which a logical identity is needed.

---

##### `RegionalFact` <a name="RegionalFact" id="cdk-constructs.ThronAcmCertificate.regionalFact"></a>

```go
func RegionalFact(factName *string, defaultValue *string) *string
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

- *Type:* *string

---

###### `defaultValue`<sup>Optional</sup> <a name="defaultValue" id="cdk-constructs.ThronAcmCertificate.regionalFact.parameter.defaultValue"></a>

- *Type:* *string

---

##### `RenameLogicalId` <a name="RenameLogicalId" id="cdk-constructs.ThronAcmCertificate.renameLogicalId"></a>

```go
func RenameLogicalId(oldId *string, newId *string)
```

Rename a generated logical identities.

To modify the naming scheme strategy, extend the `Stack` class and
override the `allocateLogicalId` method.

###### `oldId`<sup>Required</sup> <a name="oldId" id="cdk-constructs.ThronAcmCertificate.renameLogicalId.parameter.oldId"></a>

- *Type:* *string

---

###### `newId`<sup>Required</sup> <a name="newId" id="cdk-constructs.ThronAcmCertificate.renameLogicalId.parameter.newId"></a>

- *Type:* *string

---

##### `ReportMissingContextKey` <a name="ReportMissingContextKey" id="cdk-constructs.ThronAcmCertificate.reportMissingContextKey"></a>

```go
func ReportMissingContextKey(report MissingContext)
```

Indicate that a context key was expected.

Contains instructions which will be emitted into the cloud assembly on how
the key should be supplied.

###### `report`<sup>Required</sup> <a name="report" id="cdk-constructs.ThronAcmCertificate.reportMissingContextKey.parameter.report"></a>

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.cloud_assembly_schema.MissingContext

The set of parameters needed to obtain the context.

---

##### `Resolve` <a name="Resolve" id="cdk-constructs.ThronAcmCertificate.resolve"></a>

```go
func Resolve(obj interface{}) interface{}
```

Resolve a tokenized value in the context of the current stack.

###### `obj`<sup>Required</sup> <a name="obj" id="cdk-constructs.ThronAcmCertificate.resolve.parameter.obj"></a>

- *Type:* interface{}

---

##### `SplitArn` <a name="SplitArn" id="cdk-constructs.ThronAcmCertificate.splitArn"></a>

```go
func SplitArn(arn *string, arnFormat ArnFormat) ArnComponents
```

Splits the provided ARN into its components.

Works both if 'arn' is a string like 'arn:aws:s3:::bucket',
and a Token representing a dynamic CloudFormation expression
(in which case the returned components will also be dynamic CloudFormation expressions,
encoded as Tokens).

###### `arn`<sup>Required</sup> <a name="arn" id="cdk-constructs.ThronAcmCertificate.splitArn.parameter.arn"></a>

- *Type:* *string

the ARN to split into its components.

---

###### `arnFormat`<sup>Required</sup> <a name="arnFormat" id="cdk-constructs.ThronAcmCertificate.splitArn.parameter.arnFormat"></a>

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.ArnFormat

the expected format of 'arn' - depends on what format the service 'arn' represents uses.

---

##### `ToJsonString` <a name="ToJsonString" id="cdk-constructs.ThronAcmCertificate.toJsonString"></a>

```go
func ToJsonString(obj interface{}, space *f64) *string
```

Convert an object, potentially containing tokens, to a JSON string.

###### `obj`<sup>Required</sup> <a name="obj" id="cdk-constructs.ThronAcmCertificate.toJsonString.parameter.obj"></a>

- *Type:* interface{}

---

###### `space`<sup>Optional</sup> <a name="space" id="cdk-constructs.ThronAcmCertificate.toJsonString.parameter.space"></a>

- *Type:* *f64

---

##### `ToYamlString` <a name="ToYamlString" id="cdk-constructs.ThronAcmCertificate.toYamlString"></a>

```go
func ToYamlString(obj interface{}) *string
```

Convert an object, potentially containing tokens, to a YAML string.

###### `obj`<sup>Required</sup> <a name="obj" id="cdk-constructs.ThronAcmCertificate.toYamlString.parameter.obj"></a>

- *Type:* interface{}

---

#### Static Functions <a name="Static Functions" id="Static Functions"></a>

| **Name** | **Description** |
| --- | --- |
| <code><a href="#cdk-constructs.ThronAcmCertificate.isConstruct">IsConstruct</a></code> | Checks if `x` is a construct. |
| <code><a href="#cdk-constructs.ThronAcmCertificate.isStack">IsStack</a></code> | Return whether the given object is a Stack. |
| <code><a href="#cdk-constructs.ThronAcmCertificate.of">Of</a></code> | Looks up the first stack scope in which `construct` is defined. |

---

##### `IsConstruct` <a name="IsConstruct" id="cdk-constructs.ThronAcmCertificate.isConstruct"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

cdkconstructs.ThronAcmCertificate_IsConstruct(x interface{}) *bool
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

- *Type:* interface{}

Any object.

---

##### `IsStack` <a name="IsStack" id="cdk-constructs.ThronAcmCertificate.isStack"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

cdkconstructs.ThronAcmCertificate_IsStack(x interface{}) *bool
```

Return whether the given object is a Stack.

We do attribute detection since we can't reliably use 'instanceof'.

###### `x`<sup>Required</sup> <a name="x" id="cdk-constructs.ThronAcmCertificate.isStack.parameter.x"></a>

- *Type:* interface{}

---

##### `Of` <a name="Of" id="cdk-constructs.ThronAcmCertificate.of"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

cdkconstructs.ThronAcmCertificate_Of(construct IConstruct) Stack
```

Looks up the first stack scope in which `construct` is defined.

Fails if there is no stack up the tree.

###### `construct`<sup>Required</sup> <a name="construct" id="cdk-constructs.ThronAcmCertificate.of.parameter.construct"></a>

- *Type:* github.com/aws/constructs-go/constructs/v10.IConstruct

The construct to start the search from.

---

#### Properties <a name="Properties" id="Properties"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.ThronAcmCertificate.property.node">Node</a></code> | <code>github.com/aws/constructs-go/constructs/v10.Node</code> | The tree node. |
| <code><a href="#cdk-constructs.ThronAcmCertificate.property.account">Account</a></code> | <code>*string</code> | The AWS account into which this stack will be deployed. |
| <code><a href="#cdk-constructs.ThronAcmCertificate.property.artifactId">ArtifactId</a></code> | <code>*string</code> | The ID of the cloud assembly artifact for this stack. |
| <code><a href="#cdk-constructs.ThronAcmCertificate.property.availabilityZones">AvailabilityZones</a></code> | <code>*[]*string</code> | Returns the list of AZs that are available in the AWS environment (account/region) associated with this stack. |
| <code><a href="#cdk-constructs.ThronAcmCertificate.property.bundlingRequired">BundlingRequired</a></code> | <code>*bool</code> | Indicates whether the stack requires bundling or not. |
| <code><a href="#cdk-constructs.ThronAcmCertificate.property.dependencies">Dependencies</a></code> | <code>*[]github.com/aws/aws-cdk-go/awscdk/v2.Stack</code> | Return the stacks this stack depends on. |
| <code><a href="#cdk-constructs.ThronAcmCertificate.property.environment">Environment</a></code> | <code>*string</code> | The environment coordinates in which this stack is deployed. |
| <code><a href="#cdk-constructs.ThronAcmCertificate.property.nested">Nested</a></code> | <code>*bool</code> | Indicates if this is a nested stack, in which case `parentStack` will include a reference to it's parent. |
| <code><a href="#cdk-constructs.ThronAcmCertificate.property.notificationArns">NotificationArns</a></code> | <code>*[]*string</code> | Returns the list of notification Amazon Resource Names (ARNs) for the current stack. |
| <code><a href="#cdk-constructs.ThronAcmCertificate.property.partition">Partition</a></code> | <code>*string</code> | The partition in which this stack is defined. |
| <code><a href="#cdk-constructs.ThronAcmCertificate.property.region">Region</a></code> | <code>*string</code> | The AWS region into which this stack will be deployed (e.g. `us-west-2`). |
| <code><a href="#cdk-constructs.ThronAcmCertificate.property.stackId">StackId</a></code> | <code>*string</code> | The ID of the stack. |
| <code><a href="#cdk-constructs.ThronAcmCertificate.property.stackName">StackName</a></code> | <code>*string</code> | The concrete CloudFormation physical stack name. |
| <code><a href="#cdk-constructs.ThronAcmCertificate.property.synthesizer">Synthesizer</a></code> | <code>github.com/aws/aws-cdk-go/awscdk/v2.IStackSynthesizer</code> | Synthesis method for this stack. |
| <code><a href="#cdk-constructs.ThronAcmCertificate.property.tags">Tags</a></code> | <code>github.com/aws/aws-cdk-go/awscdk/v2.TagManager</code> | Tags to be applied to the stack. |
| <code><a href="#cdk-constructs.ThronAcmCertificate.property.templateFile">TemplateFile</a></code> | <code>*string</code> | The name of the CloudFormation template file emitted to the output directory during synthesis. |
| <code><a href="#cdk-constructs.ThronAcmCertificate.property.templateOptions">TemplateOptions</a></code> | <code>github.com/aws/aws-cdk-go/awscdk/v2.ITemplateOptions</code> | Options for CloudFormation template (like version, transform, description). |
| <code><a href="#cdk-constructs.ThronAcmCertificate.property.urlSuffix">UrlSuffix</a></code> | <code>*string</code> | The Amazon domain suffix for the region in which this stack is defined. |
| <code><a href="#cdk-constructs.ThronAcmCertificate.property.nestedStackParent">NestedStackParent</a></code> | <code>github.com/aws/aws-cdk-go/awscdk/v2.Stack</code> | If this is a nested stack, returns it's parent stack. |
| <code><a href="#cdk-constructs.ThronAcmCertificate.property.nestedStackResource">NestedStackResource</a></code> | <code>github.com/aws/aws-cdk-go/awscdk/v2.CfnResource</code> | If this is a nested stack, this represents its `AWS::CloudFormation::Stack` resource. |
| <code><a href="#cdk-constructs.ThronAcmCertificate.property.terminationProtection">TerminationProtection</a></code> | <code>*bool</code> | Whether termination protection is enabled for this stack. |
| <code><a href="#cdk-constructs.ThronAcmCertificate.property.certificate">Certificate</a></code> | <code>github.com/aws/aws-cdk-go/awscdk/v2.aws_certificatemanager.Certificate</code> | The issued certificate. |
| <code><a href="#cdk-constructs.ThronAcmCertificate.property.domainName">DomainName</a></code> | <code>*string</code> | FQDN the certificate is issued for. |
| <code><a href="#cdk-constructs.ThronAcmCertificate.property.subjectAlternativeNames">SubjectAlternativeNames</a></code> | <code>*[]*string</code> | Alternative domain names on the certificate. |

---

##### `Node`<sup>Required</sup> <a name="Node" id="cdk-constructs.ThronAcmCertificate.property.node"></a>

```go
func Node() Node
```

- *Type:* github.com/aws/constructs-go/constructs/v10.Node

The tree node.

---

##### `Account`<sup>Required</sup> <a name="Account" id="cdk-constructs.ThronAcmCertificate.property.account"></a>

```go
func Account() *string
```

- *Type:* *string

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

##### `ArtifactId`<sup>Required</sup> <a name="ArtifactId" id="cdk-constructs.ThronAcmCertificate.property.artifactId"></a>

```go
func ArtifactId() *string
```

- *Type:* *string

The ID of the cloud assembly artifact for this stack.

---

##### `AvailabilityZones`<sup>Required</sup> <a name="AvailabilityZones" id="cdk-constructs.ThronAcmCertificate.property.availabilityZones"></a>

```go
func AvailabilityZones() *[]*string
```

- *Type:* *[]*string

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

##### `BundlingRequired`<sup>Required</sup> <a name="BundlingRequired" id="cdk-constructs.ThronAcmCertificate.property.bundlingRequired"></a>

```go
func BundlingRequired() *bool
```

- *Type:* *bool

Indicates whether the stack requires bundling or not.

---

##### `Dependencies`<sup>Required</sup> <a name="Dependencies" id="cdk-constructs.ThronAcmCertificate.property.dependencies"></a>

```go
func Dependencies() *[]Stack
```

- *Type:* *[]github.com/aws/aws-cdk-go/awscdk/v2.Stack

Return the stacks this stack depends on.

---

##### `Environment`<sup>Required</sup> <a name="Environment" id="cdk-constructs.ThronAcmCertificate.property.environment"></a>

```go
func Environment() *string
```

- *Type:* *string

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

##### `Nested`<sup>Required</sup> <a name="Nested" id="cdk-constructs.ThronAcmCertificate.property.nested"></a>

```go
func Nested() *bool
```

- *Type:* *bool

Indicates if this is a nested stack, in which case `parentStack` will include a reference to it's parent.

---

##### `NotificationArns`<sup>Required</sup> <a name="NotificationArns" id="cdk-constructs.ThronAcmCertificate.property.notificationArns"></a>

```go
func NotificationArns() *[]*string
```

- *Type:* *[]*string

Returns the list of notification Amazon Resource Names (ARNs) for the current stack.

---

##### `Partition`<sup>Required</sup> <a name="Partition" id="cdk-constructs.ThronAcmCertificate.property.partition"></a>

```go
func Partition() *string
```

- *Type:* *string

The partition in which this stack is defined.

---

##### `Region`<sup>Required</sup> <a name="Region" id="cdk-constructs.ThronAcmCertificate.property.region"></a>

```go
func Region() *string
```

- *Type:* *string

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

##### `StackId`<sup>Required</sup> <a name="StackId" id="cdk-constructs.ThronAcmCertificate.property.stackId"></a>

```go
func StackId() *string
```

- *Type:* *string

The ID of the stack.

---

*Example*

```go
// After resolving, looks like
'arn:aws:cloudformation:us-west-2:123456789012:stack/teststack/51af3dc0-da77-11e4-872e-1234567db123'
```


##### `StackName`<sup>Required</sup> <a name="StackName" id="cdk-constructs.ThronAcmCertificate.property.stackName"></a>

```go
func StackName() *string
```

- *Type:* *string

The concrete CloudFormation physical stack name.

This is either the name defined explicitly in the `stackName` prop or
allocated based on the stack's location in the construct tree. Stacks that
are directly defined under the app use their construct `id` as their stack
name. Stacks that are defined deeper within the tree will use a hashed naming
scheme based on the construct path to ensure uniqueness.

If you wish to obtain the deploy-time AWS::StackName intrinsic,
you can use `Aws.STACK_NAME` directly.

---

##### `Synthesizer`<sup>Required</sup> <a name="Synthesizer" id="cdk-constructs.ThronAcmCertificate.property.synthesizer"></a>

```go
func Synthesizer() IStackSynthesizer
```

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.IStackSynthesizer

Synthesis method for this stack.

---

##### `Tags`<sup>Required</sup> <a name="Tags" id="cdk-constructs.ThronAcmCertificate.property.tags"></a>

```go
func Tags() TagManager
```

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.TagManager

Tags to be applied to the stack.

---

##### `TemplateFile`<sup>Required</sup> <a name="TemplateFile" id="cdk-constructs.ThronAcmCertificate.property.templateFile"></a>

```go
func TemplateFile() *string
```

- *Type:* *string

The name of the CloudFormation template file emitted to the output directory during synthesis.

Example value: `MyStack.template.json`

---

##### `TemplateOptions`<sup>Required</sup> <a name="TemplateOptions" id="cdk-constructs.ThronAcmCertificate.property.templateOptions"></a>

```go
func TemplateOptions() ITemplateOptions
```

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.ITemplateOptions

Options for CloudFormation template (like version, transform, description).

---

##### `UrlSuffix`<sup>Required</sup> <a name="UrlSuffix" id="cdk-constructs.ThronAcmCertificate.property.urlSuffix"></a>

```go
func UrlSuffix() *string
```

- *Type:* *string

The Amazon domain suffix for the region in which this stack is defined.

---

##### `NestedStackParent`<sup>Optional</sup> <a name="NestedStackParent" id="cdk-constructs.ThronAcmCertificate.property.nestedStackParent"></a>

```go
func NestedStackParent() Stack
```

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.Stack

If this is a nested stack, returns it's parent stack.

---

##### `NestedStackResource`<sup>Optional</sup> <a name="NestedStackResource" id="cdk-constructs.ThronAcmCertificate.property.nestedStackResource"></a>

```go
func NestedStackResource() CfnResource
```

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.CfnResource

If this is a nested stack, this represents its `AWS::CloudFormation::Stack` resource.

`undefined` for top-level (non-nested) stacks.

---

##### `TerminationProtection`<sup>Required</sup> <a name="TerminationProtection" id="cdk-constructs.ThronAcmCertificate.property.terminationProtection"></a>

```go
func TerminationProtection() *bool
```

- *Type:* *bool

Whether termination protection is enabled for this stack.

---

##### `Certificate`<sup>Required</sup> <a name="Certificate" id="cdk-constructs.ThronAcmCertificate.property.certificate"></a>

```go
func Certificate() Certificate
```

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_certificatemanager.Certificate

The issued certificate.

---

##### `DomainName`<sup>Required</sup> <a name="DomainName" id="cdk-constructs.ThronAcmCertificate.property.domainName"></a>

```go
func DomainName() *string
```

- *Type:* *string

FQDN the certificate is issued for.

---

##### `SubjectAlternativeNames`<sup>Optional</sup> <a name="SubjectAlternativeNames" id="cdk-constructs.ThronAcmCertificate.property.subjectAlternativeNames"></a>

```go
func SubjectAlternativeNames() *[]*string
```

- *Type:* *[]*string

Alternative domain names on the certificate.

---


### ThronApiGatewayApi <a name="ThronApiGatewayApi" id="cdk-constructs.ThronApiGatewayApi"></a>

#### Initializers <a name="Initializers" id="cdk-constructs.ThronApiGatewayApi.Initializer"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

cdkconstructs.NewThronApiGatewayApi(scope Construct, id *string, props ThronApiGatewayApiProps) ThronApiGatewayApi
```

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.ThronApiGatewayApi.Initializer.parameter.scope">scope</a></code> | <code>github.com/aws/constructs-go/constructs/v10.Construct</code> | *No description.* |
| <code><a href="#cdk-constructs.ThronApiGatewayApi.Initializer.parameter.id">id</a></code> | <code>*string</code> | *No description.* |
| <code><a href="#cdk-constructs.ThronApiGatewayApi.Initializer.parameter.props">props</a></code> | <code><a href="#cdk-constructs.ThronApiGatewayApiProps">ThronApiGatewayApiProps</a></code> | *No description.* |

---

##### `scope`<sup>Required</sup> <a name="scope" id="cdk-constructs.ThronApiGatewayApi.Initializer.parameter.scope"></a>

- *Type:* github.com/aws/constructs-go/constructs/v10.Construct

---

##### `id`<sup>Required</sup> <a name="id" id="cdk-constructs.ThronApiGatewayApi.Initializer.parameter.id"></a>

- *Type:* *string

---

##### `props`<sup>Required</sup> <a name="props" id="cdk-constructs.ThronApiGatewayApi.Initializer.parameter.props"></a>

- *Type:* <a href="#cdk-constructs.ThronApiGatewayApiProps">ThronApiGatewayApiProps</a>

---

#### Methods <a name="Methods" id="Methods"></a>

| **Name** | **Description** |
| --- | --- |
| <code><a href="#cdk-constructs.ThronApiGatewayApi.toString">ToString</a></code> | Returns a string representation of this construct. |
| <code><a href="#cdk-constructs.ThronApiGatewayApi.addAltDomain">AddAltDomain</a></code> | *No description.* |
| <code><a href="#cdk-constructs.ThronApiGatewayApi.addLambdaEndpoint">AddLambdaEndpoint</a></code> | *No description.* |
| <code><a href="#cdk-constructs.ThronApiGatewayApi.addServiceLambdaEndpoint">AddServiceLambdaEndpoint</a></code> | *No description.* |

---

##### `ToString` <a name="ToString" id="cdk-constructs.ThronApiGatewayApi.toString"></a>

```go
func ToString() *string
```

Returns a string representation of this construct.

##### `AddAltDomain` <a name="AddAltDomain" id="cdk-constructs.ThronApiGatewayApi.addAltDomain"></a>

```go
func AddAltDomain(domainFirstPart *string)
```

###### `domainFirstPart`<sup>Required</sup> <a name="domainFirstPart" id="cdk-constructs.ThronApiGatewayApi.addAltDomain.parameter.domainFirstPart"></a>

- *Type:* *string

---

##### `AddLambdaEndpoint` <a name="AddLambdaEndpoint" id="cdk-constructs.ThronApiGatewayApi.addLambdaEndpoint"></a>

```go
func AddLambdaEndpoint(lambdaFunction IFunction, basePath *string, timeout Duration) ThronEndpointApiGateway
```

###### `lambdaFunction`<sup>Required</sup> <a name="lambdaFunction" id="cdk-constructs.ThronApiGatewayApi.addLambdaEndpoint.parameter.lambdaFunction"></a>

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_lambda.IFunction

---

###### `basePath`<sup>Required</sup> <a name="basePath" id="cdk-constructs.ThronApiGatewayApi.addLambdaEndpoint.parameter.basePath"></a>

- *Type:* *string

---

###### `timeout`<sup>Required</sup> <a name="timeout" id="cdk-constructs.ThronApiGatewayApi.addLambdaEndpoint.parameter.timeout"></a>

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.Duration

---

##### `AddServiceLambdaEndpoint` <a name="AddServiceLambdaEndpoint" id="cdk-constructs.ThronApiGatewayApi.addServiceLambdaEndpoint"></a>

```go
func AddServiceLambdaEndpoint(lambdaFunction IFunction, timeout Duration, __2 FullServiceProps) ThronEndpointApiGateway
```

###### `lambdaFunction`<sup>Required</sup> <a name="lambdaFunction" id="cdk-constructs.ThronApiGatewayApi.addServiceLambdaEndpoint.parameter.lambdaFunction"></a>

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_lambda.IFunction

---

###### `timeout`<sup>Required</sup> <a name="timeout" id="cdk-constructs.ThronApiGatewayApi.addServiceLambdaEndpoint.parameter.timeout"></a>

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.Duration

---

###### `__2`<sup>Required</sup> <a name="__2" id="cdk-constructs.ThronApiGatewayApi.addServiceLambdaEndpoint.parameter.__2"></a>

- *Type:* <a href="#cdk-constructs.FullServiceProps">FullServiceProps</a>

---

#### Static Functions <a name="Static Functions" id="Static Functions"></a>

| **Name** | **Description** |
| --- | --- |
| <code><a href="#cdk-constructs.ThronApiGatewayApi.isConstruct">IsConstruct</a></code> | Checks if `x` is a construct. |
| <code><a href="#cdk-constructs.ThronApiGatewayApi.buildServiceEndpoint">BuildServiceEndpoint</a></code> | *No description.* |

---

##### `IsConstruct` <a name="IsConstruct" id="cdk-constructs.ThronApiGatewayApi.isConstruct"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

cdkconstructs.ThronApiGatewayApi_IsConstruct(x interface{}) *bool
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

- *Type:* interface{}

Any object.

---

##### `BuildServiceEndpoint` <a name="BuildServiceEndpoint" id="cdk-constructs.ThronApiGatewayApi.buildServiceEndpoint"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

cdkconstructs.ThronApiGatewayApi_BuildServiceEndpoint(scope Construct, serviceProps FullServiceProps) EndpointComponents
```

###### `scope`<sup>Required</sup> <a name="scope" id="cdk-constructs.ThronApiGatewayApi.buildServiceEndpoint.parameter.scope"></a>

- *Type:* github.com/aws/constructs-go/constructs/v10.Construct

---

###### `serviceProps`<sup>Required</sup> <a name="serviceProps" id="cdk-constructs.ThronApiGatewayApi.buildServiceEndpoint.parameter.serviceProps"></a>

- *Type:* <a href="#cdk-constructs.FullServiceProps">FullServiceProps</a>

---

#### Properties <a name="Properties" id="Properties"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.ThronApiGatewayApi.property.node">Node</a></code> | <code>github.com/aws/constructs-go/constructs/v10.Node</code> | The tree node. |
| <code><a href="#cdk-constructs.ThronApiGatewayApi.property.apiGatewayApi">ApiGatewayApi</a></code> | <code>github.com/aws/aws-cdk-go/awscdk/v2.aws_apigateway.RestApi</code> | *No description.* |
| <code><a href="#cdk-constructs.ThronApiGatewayApi.property.domainAliases">DomainAliases</a></code> | <code>*[]<a href="#cdk-constructs.ThronApiGatewayDomainAlias">ThronApiGatewayDomainAlias</a></code> | *No description.* |
| <code><a href="#cdk-constructs.ThronApiGatewayApi.property.mainDomain">MainDomain</a></code> | <code><a href="#cdk-constructs.ThronApiGatewayDomainAlias">ThronApiGatewayDomainAlias</a></code> | *No description.* |

---

##### `Node`<sup>Required</sup> <a name="Node" id="cdk-constructs.ThronApiGatewayApi.property.node"></a>

```go
func Node() Node
```

- *Type:* github.com/aws/constructs-go/constructs/v10.Node

The tree node.

---

##### `ApiGatewayApi`<sup>Required</sup> <a name="ApiGatewayApi" id="cdk-constructs.ThronApiGatewayApi.property.apiGatewayApi"></a>

```go
func ApiGatewayApi() RestApi
```

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_apigateway.RestApi

---

##### `DomainAliases`<sup>Required</sup> <a name="DomainAliases" id="cdk-constructs.ThronApiGatewayApi.property.domainAliases"></a>

```go
func DomainAliases() *[]ThronApiGatewayDomainAlias
```

- *Type:* *[]<a href="#cdk-constructs.ThronApiGatewayDomainAlias">ThronApiGatewayDomainAlias</a>

---

##### `MainDomain`<sup>Required</sup> <a name="MainDomain" id="cdk-constructs.ThronApiGatewayApi.property.mainDomain"></a>

```go
func MainDomain() ThronApiGatewayDomainAlias
```

- *Type:* <a href="#cdk-constructs.ThronApiGatewayDomainAlias">ThronApiGatewayDomainAlias</a>

---


### ThronApiGatewayDomainAlias <a name="ThronApiGatewayDomainAlias" id="cdk-constructs.ThronApiGatewayDomainAlias"></a>

Defines an Alias domain to the main api-gateway.

*Example*

```go
// Example automatically generated from non-compiling source. May contain errors.
endpoint := NewThronApiGatewayDomainAlias(this, jsii.String("cool-domain-alias"), map[string]interface{}{
	"domainName": jsii.String("cool-domain.4me.cdndev.weebo.it"),
	"apiGatewayApi": sampleApi.restApiId,
	"domainId": jsii.String("cool-domain"),
})
```


#### Initializers <a name="Initializers" id="cdk-constructs.ThronApiGatewayDomainAlias.Initializer"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

cdkconstructs.NewThronApiGatewayDomainAlias(scope Construct, id *string, props ThronApiGatewayDomainAliasProps) ThronApiGatewayDomainAlias
```

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.ThronApiGatewayDomainAlias.Initializer.parameter.scope">scope</a></code> | <code>github.com/aws/constructs-go/constructs/v10.Construct</code> | *No description.* |
| <code><a href="#cdk-constructs.ThronApiGatewayDomainAlias.Initializer.parameter.id">id</a></code> | <code>*string</code> | *No description.* |
| <code><a href="#cdk-constructs.ThronApiGatewayDomainAlias.Initializer.parameter.props">props</a></code> | <code><a href="#cdk-constructs.ThronApiGatewayDomainAliasProps">ThronApiGatewayDomainAliasProps</a></code> | *No description.* |

---

##### `scope`<sup>Required</sup> <a name="scope" id="cdk-constructs.ThronApiGatewayDomainAlias.Initializer.parameter.scope"></a>

- *Type:* github.com/aws/constructs-go/constructs/v10.Construct

---

##### `id`<sup>Required</sup> <a name="id" id="cdk-constructs.ThronApiGatewayDomainAlias.Initializer.parameter.id"></a>

- *Type:* *string

---

##### `props`<sup>Required</sup> <a name="props" id="cdk-constructs.ThronApiGatewayDomainAlias.Initializer.parameter.props"></a>

- *Type:* <a href="#cdk-constructs.ThronApiGatewayDomainAliasProps">ThronApiGatewayDomainAliasProps</a>

---

#### Methods <a name="Methods" id="Methods"></a>

| **Name** | **Description** |
| --- | --- |
| <code><a href="#cdk-constructs.ThronApiGatewayDomainAlias.toString">ToString</a></code> | Returns a string representation of this construct. |

---

##### `ToString` <a name="ToString" id="cdk-constructs.ThronApiGatewayDomainAlias.toString"></a>

```go
func ToString() *string
```

Returns a string representation of this construct.

#### Static Functions <a name="Static Functions" id="Static Functions"></a>

| **Name** | **Description** |
| --- | --- |
| <code><a href="#cdk-constructs.ThronApiGatewayDomainAlias.isConstruct">IsConstruct</a></code> | Checks if `x` is a construct. |

---

##### `IsConstruct` <a name="IsConstruct" id="cdk-constructs.ThronApiGatewayDomainAlias.isConstruct"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

cdkconstructs.ThronApiGatewayDomainAlias_IsConstruct(x interface{}) *bool
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

- *Type:* interface{}

Any object.

---

#### Properties <a name="Properties" id="Properties"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.ThronApiGatewayDomainAlias.property.node">Node</a></code> | <code>github.com/aws/constructs-go/constructs/v10.Node</code> | The tree node. |
| <code><a href="#cdk-constructs.ThronApiGatewayDomainAlias.property.recordName">RecordName</a></code> | <code>*string</code> | *No description.* |

---

##### `Node`<sup>Required</sup> <a name="Node" id="cdk-constructs.ThronApiGatewayDomainAlias.property.node"></a>

```go
func Node() Node
```

- *Type:* github.com/aws/constructs-go/constructs/v10.Node

The tree node.

---

##### `RecordName`<sup>Required</sup> <a name="RecordName" id="cdk-constructs.ThronApiGatewayDomainAlias.property.recordName"></a>

```go
func RecordName() *string
```

- *Type:* *string

---


### ThronCachePolicy <a name="ThronCachePolicy" id="cdk-constructs.ThronCachePolicy"></a>

#### Methods <a name="Methods" id="Methods"></a>

| **Name** | **Description** |
| --- | --- |
| <code><a href="#cdk-constructs.ThronCachePolicy.toString">ToString</a></code> | Returns a string representation of this construct. |
| <code><a href="#cdk-constructs.ThronCachePolicy.applyRemovalPolicy">ApplyRemovalPolicy</a></code> | Apply the given removal policy to this resource. |

---

##### `ToString` <a name="ToString" id="cdk-constructs.ThronCachePolicy.toString"></a>

```go
func ToString() *string
```

Returns a string representation of this construct.

##### `ApplyRemovalPolicy` <a name="ApplyRemovalPolicy" id="cdk-constructs.ThronCachePolicy.applyRemovalPolicy"></a>

```go
func ApplyRemovalPolicy(policy RemovalPolicy)
```

Apply the given removal policy to this resource.

The Removal Policy controls what happens to this resource when it stops
being managed by CloudFormation, either because you've removed it from the
CDK application or because you've made a change that requires the resource
to be replaced.

The resource can be deleted (`RemovalPolicy.DESTROY`), or left in your AWS
account for data recovery and cleanup later (`RemovalPolicy.RETAIN`).

###### `policy`<sup>Required</sup> <a name="policy" id="cdk-constructs.ThronCachePolicy.applyRemovalPolicy.parameter.policy"></a>

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.RemovalPolicy

---

#### Static Functions <a name="Static Functions" id="Static Functions"></a>

| **Name** | **Description** |
| --- | --- |
| <code><a href="#cdk-constructs.ThronCachePolicy.isConstruct">IsConstruct</a></code> | Checks if `x` is a construct. |
| <code><a href="#cdk-constructs.ThronCachePolicy.isOwnedResource">IsOwnedResource</a></code> | Returns true if the construct was created by CDK, and false otherwise. |
| <code><a href="#cdk-constructs.ThronCachePolicy.isResource">IsResource</a></code> | Check whether the given construct is a Resource. |
| <code><a href="#cdk-constructs.ThronCachePolicy.fromCachePolicyId">FromCachePolicyId</a></code> | Imports a Cache Policy from its id. |
| <code><a href="#cdk-constructs.ThronCachePolicy.cacheDisabled">CacheDisabled</a></code> | *No description.* |
| <code><a href="#cdk-constructs.ThronCachePolicy.default">Default</a></code> | Generates a `ThronCachePolicy` with all the default values. |
| <code><a href="#cdk-constructs.ThronCachePolicy.defaultWithOverrides">DefaultWithOverrides</a></code> | Generates a `ThronCachePolicy` with all the default values except for the ones passed on `props`. |

---

##### `IsConstruct` <a name="IsConstruct" id="cdk-constructs.ThronCachePolicy.isConstruct"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

cdkconstructs.ThronCachePolicy_IsConstruct(x interface{}) *bool
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

- *Type:* interface{}

Any object.

---

##### `IsOwnedResource` <a name="IsOwnedResource" id="cdk-constructs.ThronCachePolicy.isOwnedResource"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

cdkconstructs.ThronCachePolicy_IsOwnedResource(construct IConstruct) *bool
```

Returns true if the construct was created by CDK, and false otherwise.

###### `construct`<sup>Required</sup> <a name="construct" id="cdk-constructs.ThronCachePolicy.isOwnedResource.parameter.construct"></a>

- *Type:* github.com/aws/constructs-go/constructs/v10.IConstruct

---

##### `IsResource` <a name="IsResource" id="cdk-constructs.ThronCachePolicy.isResource"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

cdkconstructs.ThronCachePolicy_IsResource(construct IConstruct) *bool
```

Check whether the given construct is a Resource.

###### `construct`<sup>Required</sup> <a name="construct" id="cdk-constructs.ThronCachePolicy.isResource.parameter.construct"></a>

- *Type:* github.com/aws/constructs-go/constructs/v10.IConstruct

---

##### `FromCachePolicyId` <a name="FromCachePolicyId" id="cdk-constructs.ThronCachePolicy.fromCachePolicyId"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

cdkconstructs.ThronCachePolicy_FromCachePolicyId(scope Construct, id *string, cachePolicyId *string) ICachePolicy
```

Imports a Cache Policy from its id.

###### `scope`<sup>Required</sup> <a name="scope" id="cdk-constructs.ThronCachePolicy.fromCachePolicyId.parameter.scope"></a>

- *Type:* github.com/aws/constructs-go/constructs/v10.Construct

---

###### `id`<sup>Required</sup> <a name="id" id="cdk-constructs.ThronCachePolicy.fromCachePolicyId.parameter.id"></a>

- *Type:* *string

---

###### `cachePolicyId`<sup>Required</sup> <a name="cachePolicyId" id="cdk-constructs.ThronCachePolicy.fromCachePolicyId.parameter.cachePolicyId"></a>

- *Type:* *string

---

##### `CacheDisabled` <a name="CacheDisabled" id="cdk-constructs.ThronCachePolicy.cacheDisabled"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

cdkconstructs.ThronCachePolicy_CacheDisabled(scope Construct, id *string) ThronCachePolicy
```

###### `scope`<sup>Required</sup> <a name="scope" id="cdk-constructs.ThronCachePolicy.cacheDisabled.parameter.scope"></a>

- *Type:* github.com/aws/constructs-go/constructs/v10.Construct

---

###### `id`<sup>Required</sup> <a name="id" id="cdk-constructs.ThronCachePolicy.cacheDisabled.parameter.id"></a>

- *Type:* *string

---

##### `Default` <a name="Default" id="cdk-constructs.ThronCachePolicy.default"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

cdkconstructs.ThronCachePolicy_Default(scope Construct, id *string) ThronCachePolicy
```

Generates a `ThronCachePolicy` with all the default values.

###### `scope`<sup>Required</sup> <a name="scope" id="cdk-constructs.ThronCachePolicy.default.parameter.scope"></a>

- *Type:* github.com/aws/constructs-go/constructs/v10.Construct

---

###### `id`<sup>Required</sup> <a name="id" id="cdk-constructs.ThronCachePolicy.default.parameter.id"></a>

- *Type:* *string

---

##### `DefaultWithOverrides` <a name="DefaultWithOverrides" id="cdk-constructs.ThronCachePolicy.defaultWithOverrides"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

cdkconstructs.ThronCachePolicy_DefaultWithOverrides(scope Construct, id *string, props ThronCachePolicyProps) ThronCachePolicy
```

Generates a `ThronCachePolicy` with all the default values except for the ones passed on `props`.

###### `scope`<sup>Required</sup> <a name="scope" id="cdk-constructs.ThronCachePolicy.defaultWithOverrides.parameter.scope"></a>

- *Type:* github.com/aws/constructs-go/constructs/v10.Construct

---

###### `id`<sup>Required</sup> <a name="id" id="cdk-constructs.ThronCachePolicy.defaultWithOverrides.parameter.id"></a>

- *Type:* *string

---

###### `props`<sup>Required</sup> <a name="props" id="cdk-constructs.ThronCachePolicy.defaultWithOverrides.parameter.props"></a>

- *Type:* <a href="#cdk-constructs.ThronCachePolicyProps">ThronCachePolicyProps</a>

---

#### Properties <a name="Properties" id="Properties"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.ThronCachePolicy.property.node">Node</a></code> | <code>github.com/aws/constructs-go/constructs/v10.Node</code> | The tree node. |
| <code><a href="#cdk-constructs.ThronCachePolicy.property.env">Env</a></code> | <code>github.com/aws/aws-cdk-go/awscdk/v2.ResourceEnvironment</code> | The environment this resource belongs to. |
| <code><a href="#cdk-constructs.ThronCachePolicy.property.stack">Stack</a></code> | <code>github.com/aws/aws-cdk-go/awscdk/v2.Stack</code> | The stack in which this resource is defined. |
| <code><a href="#cdk-constructs.ThronCachePolicy.property.cachePolicyId">CachePolicyId</a></code> | <code>*string</code> | The ID of the cache policy. |

---

##### `Node`<sup>Required</sup> <a name="Node" id="cdk-constructs.ThronCachePolicy.property.node"></a>

```go
func Node() Node
```

- *Type:* github.com/aws/constructs-go/constructs/v10.Node

The tree node.

---

##### `Env`<sup>Required</sup> <a name="Env" id="cdk-constructs.ThronCachePolicy.property.env"></a>

```go
func Env() ResourceEnvironment
```

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.ResourceEnvironment

The environment this resource belongs to.

For resources that are created and managed by the CDK
(generally, those created by creating new class instances like Role, Bucket, etc.),
this is always the same as the environment of the stack they belong to;
however, for imported resources
(those obtained from static methods like fromRoleArn, fromBucketName, etc.),
that might be different than the stack they were imported into.

---

##### `Stack`<sup>Required</sup> <a name="Stack" id="cdk-constructs.ThronCachePolicy.property.stack"></a>

```go
func Stack() Stack
```

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.Stack

The stack in which this resource is defined.

---

##### `CachePolicyId`<sup>Required</sup> <a name="CachePolicyId" id="cdk-constructs.ThronCachePolicy.property.cachePolicyId"></a>

```go
func CachePolicyId() *string
```

- *Type:* *string

The ID of the cache policy.

---

#### Constants <a name="Constants" id="Constants"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.ThronCachePolicy.property.AMPLIFY">Amplify</a></code> | <code>github.com/aws/aws-cdk-go/awscdk/v2.aws_cloudfront.ICachePolicy</code> | This policy is designed for use with an origin that is an AWS Amplify web app. |
| <code><a href="#cdk-constructs.ThronCachePolicy.property.CACHING_DISABLED">CachingDisabled</a></code> | <code>github.com/aws/aws-cdk-go/awscdk/v2.aws_cloudfront.ICachePolicy</code> | Disables caching. |
| <code><a href="#cdk-constructs.ThronCachePolicy.property.CACHING_OPTIMIZED">CachingOptimized</a></code> | <code>github.com/aws/aws-cdk-go/awscdk/v2.aws_cloudfront.ICachePolicy</code> | Optimize cache efficiency by minimizing the values that CloudFront includes in the cache key. |
| <code><a href="#cdk-constructs.ThronCachePolicy.property.CACHING_OPTIMIZED_FOR_UNCOMPRESSED_OBJECTS">CachingOptimizedForUncompressedObjects</a></code> | <code>github.com/aws/aws-cdk-go/awscdk/v2.aws_cloudfront.ICachePolicy</code> | Optimize cache efficiency by minimizing the values that CloudFront includes in the cache key. |
| <code><a href="#cdk-constructs.ThronCachePolicy.property.ELEMENTAL_MEDIA_PACKAGE">ElementalMediaPackage</a></code> | <code>github.com/aws/aws-cdk-go/awscdk/v2.aws_cloudfront.ICachePolicy</code> | Designed for use with an origin that is an AWS Elemental MediaPackage endpoint. |
| <code><a href="#cdk-constructs.ThronCachePolicy.property.USE_ORIGIN_CACHE_CONTROL_HEADERS">UseOriginCacheControlHeaders</a></code> | <code>github.com/aws/aws-cdk-go/awscdk/v2.aws_cloudfront.ICachePolicy</code> | Designed for use with an origin that returns Cache-Control HTTP response headers and does not serve different content based on values present in the query string. |
| <code><a href="#cdk-constructs.ThronCachePolicy.property.USE_ORIGIN_CACHE_CONTROL_HEADERS_QUERY_STRINGS">UseOriginCacheControlHeadersQueryStrings</a></code> | <code>github.com/aws/aws-cdk-go/awscdk/v2.aws_cloudfront.ICachePolicy</code> | Designed for use with an origin that returns Cache-Control HTTP response headers and serves different content based on values present in the query string. |

---

##### `Amplify`<sup>Required</sup> <a name="Amplify" id="cdk-constructs.ThronCachePolicy.property.AMPLIFY"></a>

```go
func Amplify() ICachePolicy
```

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_cloudfront.ICachePolicy

This policy is designed for use with an origin that is an AWS Amplify web app.

---

##### `CachingDisabled`<sup>Required</sup> <a name="CachingDisabled" id="cdk-constructs.ThronCachePolicy.property.CACHING_DISABLED"></a>

```go
func CachingDisabled() ICachePolicy
```

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_cloudfront.ICachePolicy

Disables caching.

This policy is useful for dynamic content and for requests that are not cacheable.

---

##### `CachingOptimized`<sup>Required</sup> <a name="CachingOptimized" id="cdk-constructs.ThronCachePolicy.property.CACHING_OPTIMIZED"></a>

```go
func CachingOptimized() ICachePolicy
```

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_cloudfront.ICachePolicy

Optimize cache efficiency by minimizing the values that CloudFront includes in the cache key.

Query strings and cookies are not included in the cache key, and only the normalized 'Accept-Encoding' header is included.

---

##### `CachingOptimizedForUncompressedObjects`<sup>Required</sup> <a name="CachingOptimizedForUncompressedObjects" id="cdk-constructs.ThronCachePolicy.property.CACHING_OPTIMIZED_FOR_UNCOMPRESSED_OBJECTS"></a>

```go
func CachingOptimizedForUncompressedObjects() ICachePolicy
```

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_cloudfront.ICachePolicy

Optimize cache efficiency by minimizing the values that CloudFront includes in the cache key.

Query strings and cookies are not included in the cache key, and only the normalized 'Accept-Encoding' header is included.
Disables cache compression.

---

##### `ElementalMediaPackage`<sup>Required</sup> <a name="ElementalMediaPackage" id="cdk-constructs.ThronCachePolicy.property.ELEMENTAL_MEDIA_PACKAGE"></a>

```go
func ElementalMediaPackage() ICachePolicy
```

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_cloudfront.ICachePolicy

Designed for use with an origin that is an AWS Elemental MediaPackage endpoint.

---

##### `UseOriginCacheControlHeaders`<sup>Required</sup> <a name="UseOriginCacheControlHeaders" id="cdk-constructs.ThronCachePolicy.property.USE_ORIGIN_CACHE_CONTROL_HEADERS"></a>

```go
func UseOriginCacheControlHeaders() ICachePolicy
```

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_cloudfront.ICachePolicy

Designed for use with an origin that returns Cache-Control HTTP response headers and does not serve different content based on values present in the query string.

---

##### `UseOriginCacheControlHeadersQueryStrings`<sup>Required</sup> <a name="UseOriginCacheControlHeadersQueryStrings" id="cdk-constructs.ThronCachePolicy.property.USE_ORIGIN_CACHE_CONTROL_HEADERS_QUERY_STRINGS"></a>

```go
func UseOriginCacheControlHeadersQueryStrings() ICachePolicy
```

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_cloudfront.ICachePolicy

Designed for use with an origin that returns Cache-Control HTTP response headers and serves different content based on values present in the query string.

---

### ThronCloudFrontDistribution <a name="ThronCloudFrontDistribution" id="cdk-constructs.ThronCloudFrontDistribution"></a>

#### Initializers <a name="Initializers" id="cdk-constructs.ThronCloudFrontDistribution.Initializer"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

cdkconstructs.NewThronCloudFrontDistribution(scope Stack, id *string, props ThronCloudFrontDistributionProps) ThronCloudFrontDistribution
```

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.ThronCloudFrontDistribution.Initializer.parameter.scope">scope</a></code> | <code>github.com/aws/aws-cdk-go/awscdk/v2.Stack</code> | *No description.* |
| <code><a href="#cdk-constructs.ThronCloudFrontDistribution.Initializer.parameter.id">id</a></code> | <code>*string</code> | *No description.* |
| <code><a href="#cdk-constructs.ThronCloudFrontDistribution.Initializer.parameter.props">props</a></code> | <code><a href="#cdk-constructs.ThronCloudFrontDistributionProps">ThronCloudFrontDistributionProps</a></code> | *No description.* |

---

##### `scope`<sup>Required</sup> <a name="scope" id="cdk-constructs.ThronCloudFrontDistribution.Initializer.parameter.scope"></a>

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.Stack

---

##### `id`<sup>Required</sup> <a name="id" id="cdk-constructs.ThronCloudFrontDistribution.Initializer.parameter.id"></a>

- *Type:* *string

---

##### `props`<sup>Required</sup> <a name="props" id="cdk-constructs.ThronCloudFrontDistribution.Initializer.parameter.props"></a>

- *Type:* <a href="#cdk-constructs.ThronCloudFrontDistributionProps">ThronCloudFrontDistributionProps</a>

---

#### Methods <a name="Methods" id="Methods"></a>

| **Name** | **Description** |
| --- | --- |
| <code><a href="#cdk-constructs.ThronCloudFrontDistribution.toString">ToString</a></code> | Returns a string representation of this construct. |
| <code><a href="#cdk-constructs.ThronCloudFrontDistribution.isValidVersion">IsValidVersion</a></code> | Validates `version` against frontend conventions. |

---

##### `ToString` <a name="ToString" id="cdk-constructs.ThronCloudFrontDistribution.toString"></a>

```go
func ToString() *string
```

Returns a string representation of this construct.

##### `IsValidVersion` <a name="IsValidVersion" id="cdk-constructs.ThronCloudFrontDistribution.isValidVersion"></a>

```go
func IsValidVersion(version *string) *bool
```

Validates `version` against frontend conventions.

###### `version`<sup>Optional</sup> <a name="version" id="cdk-constructs.ThronCloudFrontDistribution.isValidVersion.parameter.version"></a>

- *Type:* *string

---

#### Static Functions <a name="Static Functions" id="Static Functions"></a>

| **Name** | **Description** |
| --- | --- |
| <code><a href="#cdk-constructs.ThronCloudFrontDistribution.isConstruct">IsConstruct</a></code> | Checks if `x` is a construct. |

---

##### `IsConstruct` <a name="IsConstruct" id="cdk-constructs.ThronCloudFrontDistribution.isConstruct"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

cdkconstructs.ThronCloudFrontDistribution_IsConstruct(x interface{}) *bool
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

- *Type:* interface{}

Any object.

---

#### Properties <a name="Properties" id="Properties"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.ThronCloudFrontDistribution.property.node">Node</a></code> | <code>github.com/aws/constructs-go/constructs/v10.Node</code> | The tree node. |
| <code><a href="#cdk-constructs.ThronCloudFrontDistribution.property.cachePolicy">CachePolicy</a></code> | <code>github.com/aws/aws-cdk-go/awscdk/v2.aws_cloudfront.CachePolicy</code> | Custom Cache Policy for the distribution. |
| <code><a href="#cdk-constructs.ThronCloudFrontDistribution.property.certificate">Certificate</a></code> | <code>github.com/aws/aws-cdk-go/awscdk/v2.aws_certificatemanager.Certificate</code> | Certificate used for validating the domain name. |
| <code><a href="#cdk-constructs.ThronCloudFrontDistribution.property.defaultRootObject">DefaultRootObject</a></code> | <code>*string</code> | Object that you want CloudFront to request from your origin when a user requests the root URL for your distribution. |
| <code><a href="#cdk-constructs.ThronCloudFrontDistribution.property.defaultRootObjectCachePolicy">DefaultRootObjectCachePolicy</a></code> | <code><a href="#cdk-constructs.ThronCachePolicy">ThronCachePolicy</a></code> | *No description.* |
| <code><a href="#cdk-constructs.ThronCloudFrontDistribution.property.defaultRootObjectResponseHeaderPolicy">DefaultRootObjectResponseHeaderPolicy</a></code> | <code><a href="#cdk-constructs.ThronResponseHeaderPolicy">ThronResponseHeaderPolicy</a></code> | *No description.* |
| <code><a href="#cdk-constructs.ThronCloudFrontDistribution.property.deployBucket">DeployBucket</a></code> | <code>github.com/aws/aws-cdk-go/awscdk/v2.aws_s3_deployment.BucketDeployment</code> | Populates an S3 bucket with the contents of .zip files from your local disk. |
| <code><a href="#cdk-constructs.ThronCloudFrontDistribution.property.description">Description</a></code> | <code>*string</code> | Description of the CloudFront Distribution. |
| <code><a href="#cdk-constructs.ThronCloudFrontDistribution.property.distribution">Distribution</a></code> | <code>github.com/aws/aws-cdk-go/awscdk/v2.aws_cloudfront.Distribution</code> | CloudFront distribution with associated origins and caching behaviors. |
| <code><a href="#cdk-constructs.ThronCloudFrontDistribution.property.domainName">DomainName</a></code> | <code>*string</code> | Validated FQDN. |
| <code><a href="#cdk-constructs.ThronCloudFrontDistribution.property.oac">Oac</a></code> | <code>github.com/aws/aws-cdk-go/awscdk/v2.aws_cloudfront.CfnOriginAccessControl</code> | Origin Access Control used to block public access to the S3 bucket so that users can access the content in the bucket only through CloudFront. |
| <code><a href="#cdk-constructs.ThronCloudFrontDistribution.property.responseHeaderPolicy">ResponseHeaderPolicy</a></code> | <code>github.com/aws/aws-cdk-go/awscdk/v2.aws_cloudfront.ResponseHeadersPolicy</code> | Custom Response Headers Policy. |
| <code><a href="#cdk-constructs.ThronCloudFrontDistribution.property.sourcePublicAsset">SourcePublicAsset</a></code> | <code>*string</code> | Source path from which to deploy the contents of frontend. |
| <code><a href="#cdk-constructs.ThronCloudFrontDistribution.property.version">Version</a></code> | <code>*string</code> | Prefix key used for versioning. |
| <code><a href="#cdk-constructs.ThronCloudFrontDistribution.property.websiteBucket">WebsiteBucket</a></code> | <code>github.com/aws/aws-cdk-go/awscdk/v2.aws_s3.Bucket</code> | S3 Bucket where is stored the frontend static resources. |

---

##### `Node`<sup>Required</sup> <a name="Node" id="cdk-constructs.ThronCloudFrontDistribution.property.node"></a>

```go
func Node() Node
```

- *Type:* github.com/aws/constructs-go/constructs/v10.Node

The tree node.

---

##### `CachePolicy`<sup>Required</sup> <a name="CachePolicy" id="cdk-constructs.ThronCloudFrontDistribution.property.cachePolicy"></a>

```go
func CachePolicy() CachePolicy
```

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_cloudfront.CachePolicy

Custom Cache Policy for the distribution.

---

##### `Certificate`<sup>Required</sup> <a name="Certificate" id="cdk-constructs.ThronCloudFrontDistribution.property.certificate"></a>

```go
func Certificate() Certificate
```

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_certificatemanager.Certificate

Certificate used for validating the domain name.

---

##### `DefaultRootObject`<sup>Required</sup> <a name="DefaultRootObject" id="cdk-constructs.ThronCloudFrontDistribution.property.defaultRootObject"></a>

```go
func DefaultRootObject() *string
```

- *Type:* *string

Object that you want CloudFront to request from your origin when a user requests the root URL for your distribution.

---

##### `DefaultRootObjectCachePolicy`<sup>Required</sup> <a name="DefaultRootObjectCachePolicy" id="cdk-constructs.ThronCloudFrontDistribution.property.defaultRootObjectCachePolicy"></a>

```go
func DefaultRootObjectCachePolicy() ThronCachePolicy
```

- *Type:* <a href="#cdk-constructs.ThronCachePolicy">ThronCachePolicy</a>

---

##### `DefaultRootObjectResponseHeaderPolicy`<sup>Required</sup> <a name="DefaultRootObjectResponseHeaderPolicy" id="cdk-constructs.ThronCloudFrontDistribution.property.defaultRootObjectResponseHeaderPolicy"></a>

```go
func DefaultRootObjectResponseHeaderPolicy() ThronResponseHeaderPolicy
```

- *Type:* <a href="#cdk-constructs.ThronResponseHeaderPolicy">ThronResponseHeaderPolicy</a>

---

##### `DeployBucket`<sup>Required</sup> <a name="DeployBucket" id="cdk-constructs.ThronCloudFrontDistribution.property.deployBucket"></a>

```go
func DeployBucket() BucketDeployment
```

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_s3_deployment.BucketDeployment

Populates an S3 bucket with the contents of .zip files from your local disk.

---

##### `Description`<sup>Required</sup> <a name="Description" id="cdk-constructs.ThronCloudFrontDistribution.property.description"></a>

```go
func Description() *string
```

- *Type:* *string

Description of the CloudFront Distribution.

---

##### `Distribution`<sup>Required</sup> <a name="Distribution" id="cdk-constructs.ThronCloudFrontDistribution.property.distribution"></a>

```go
func Distribution() Distribution
```

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_cloudfront.Distribution

CloudFront distribution with associated origins and caching behaviors.

---

##### `DomainName`<sup>Required</sup> <a name="DomainName" id="cdk-constructs.ThronCloudFrontDistribution.property.domainName"></a>

```go
func DomainName() *string
```

- *Type:* *string

Validated FQDN.

---

##### `Oac`<sup>Required</sup> <a name="Oac" id="cdk-constructs.ThronCloudFrontDistribution.property.oac"></a>

```go
func Oac() CfnOriginAccessControl
```

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_cloudfront.CfnOriginAccessControl

Origin Access Control used to block public access to the S3 bucket so that users can access the content in the bucket only through CloudFront.

---

##### `ResponseHeaderPolicy`<sup>Required</sup> <a name="ResponseHeaderPolicy" id="cdk-constructs.ThronCloudFrontDistribution.property.responseHeaderPolicy"></a>

```go
func ResponseHeaderPolicy() ResponseHeadersPolicy
```

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_cloudfront.ResponseHeadersPolicy

Custom Response Headers Policy.

---

##### `SourcePublicAsset`<sup>Required</sup> <a name="SourcePublicAsset" id="cdk-constructs.ThronCloudFrontDistribution.property.sourcePublicAsset"></a>

```go
func SourcePublicAsset() *string
```

- *Type:* *string

Source path from which to deploy the contents of frontend.

---

##### `Version`<sup>Required</sup> <a name="Version" id="cdk-constructs.ThronCloudFrontDistribution.property.version"></a>

```go
func Version() *string
```

- *Type:* *string

Prefix key used for versioning.

---

##### `WebsiteBucket`<sup>Required</sup> <a name="WebsiteBucket" id="cdk-constructs.ThronCloudFrontDistribution.property.websiteBucket"></a>

```go
func WebsiteBucket() Bucket
```

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_s3.Bucket

S3 Bucket where is stored the frontend static resources.

---


### ThronDockerLambda <a name="ThronDockerLambda" id="cdk-constructs.ThronDockerLambda"></a>

#### Initializers <a name="Initializers" id="cdk-constructs.ThronDockerLambda.Initializer"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

cdkconstructs.NewThronDockerLambda(scope Stack, id *string, props FunctionOptions) ThronDockerLambda
```

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.ThronDockerLambda.Initializer.parameter.scope">scope</a></code> | <code>github.com/aws/aws-cdk-go/awscdk/v2.Stack</code> | *No description.* |
| <code><a href="#cdk-constructs.ThronDockerLambda.Initializer.parameter.id">id</a></code> | <code>*string</code> | *No description.* |
| <code><a href="#cdk-constructs.ThronDockerLambda.Initializer.parameter.props">props</a></code> | <code><a href="#cdk-constructs.FunctionOptions">FunctionOptions</a></code> | *No description.* |

---

##### `scope`<sup>Required</sup> <a name="scope" id="cdk-constructs.ThronDockerLambda.Initializer.parameter.scope"></a>

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.Stack

---

##### `id`<sup>Required</sup> <a name="id" id="cdk-constructs.ThronDockerLambda.Initializer.parameter.id"></a>

- *Type:* *string

---

##### `props`<sup>Required</sup> <a name="props" id="cdk-constructs.ThronDockerLambda.Initializer.parameter.props"></a>

- *Type:* <a href="#cdk-constructs.FunctionOptions">FunctionOptions</a>

---

#### Methods <a name="Methods" id="Methods"></a>

| **Name** | **Description** |
| --- | --- |
| <code><a href="#cdk-constructs.ThronDockerLambda.toString">ToString</a></code> | Returns a string representation of this construct. |
| <code><a href="#cdk-constructs.ThronDockerLambda.applyRemovalPolicy">ApplyRemovalPolicy</a></code> | Apply the given removal policy to this resource. |
| <code><a href="#cdk-constructs.ThronDockerLambda.addEventSource">AddEventSource</a></code> | Adds an event source to this function. |
| <code><a href="#cdk-constructs.ThronDockerLambda.addEventSourceMapping">AddEventSourceMapping</a></code> | Adds an event source that maps to this AWS Lambda function. |
| <code><a href="#cdk-constructs.ThronDockerLambda.addFunctionUrl">AddFunctionUrl</a></code> | Adds a url to this lambda function. |
| <code><a href="#cdk-constructs.ThronDockerLambda.addPermission">AddPermission</a></code> | Adds a permission to the Lambda resource policy. |
| <code><a href="#cdk-constructs.ThronDockerLambda.addToRolePolicy">AddToRolePolicy</a></code> | Adds a statement to the IAM role assumed by the instance. |
| <code><a href="#cdk-constructs.ThronDockerLambda.configureAsyncInvoke">ConfigureAsyncInvoke</a></code> | Configures options for asynchronous invocation. |
| <code><a href="#cdk-constructs.ThronDockerLambda.considerWarningOnInvokeFunctionPermissions">ConsiderWarningOnInvokeFunctionPermissions</a></code> | A warning will be added to functions under the following conditions: - permissions that include `lambda:InvokeFunction` are added to the unqualified function. |
| <code><a href="#cdk-constructs.ThronDockerLambda.grantInvoke">GrantInvoke</a></code> | Grant the given identity permissions to invoke this Lambda. |
| <code><a href="#cdk-constructs.ThronDockerLambda.grantInvokeCompositePrincipal">GrantInvokeCompositePrincipal</a></code> | Grant multiple principals the ability to invoke this Lambda via CompositePrincipal. |
| <code><a href="#cdk-constructs.ThronDockerLambda.grantInvokeLatestVersion">GrantInvokeLatestVersion</a></code> | Grant the given identity permissions to invoke the $LATEST version or unqualified version of this Lambda. |
| <code><a href="#cdk-constructs.ThronDockerLambda.grantInvokeUrl">GrantInvokeUrl</a></code> | Grant the given identity permissions to invoke this Lambda Function URL. |
| <code><a href="#cdk-constructs.ThronDockerLambda.grantInvokeVersion">GrantInvokeVersion</a></code> | Grant the given identity permissions to invoke the given version of this Lambda. |
| <code><a href="#cdk-constructs.ThronDockerLambda.metric">Metric</a></code> | Return the given named metric for this Function. |
| <code><a href="#cdk-constructs.ThronDockerLambda.metricDuration">MetricDuration</a></code> | How long execution of this Lambda takes. |
| <code><a href="#cdk-constructs.ThronDockerLambda.metricErrors">MetricErrors</a></code> | How many invocations of this Lambda fail. |
| <code><a href="#cdk-constructs.ThronDockerLambda.metricInvocations">MetricInvocations</a></code> | How often this Lambda is invoked. |
| <code><a href="#cdk-constructs.ThronDockerLambda.metricThrottles">MetricThrottles</a></code> | How often this Lambda is throttled. |
| <code><a href="#cdk-constructs.ThronDockerLambda.addAlias">AddAlias</a></code> | Defines an alias for this function. |
| <code><a href="#cdk-constructs.ThronDockerLambda.addEnvironment">AddEnvironment</a></code> | Adds an environment variable to this Lambda function. |
| <code><a href="#cdk-constructs.ThronDockerLambda.addLayers">AddLayers</a></code> | Adds one or more Lambda Layers to this Lambda function. |
| <code><a href="#cdk-constructs.ThronDockerLambda.invalidateVersionBasedOn">InvalidateVersionBasedOn</a></code> | Mix additional information into the hash of the Version object. |
| <code><a href="#cdk-constructs.ThronDockerLambda.addEndpointAlb">AddEndpointAlb</a></code> | Add an endpoint the lambda function. |
| <code><a href="#cdk-constructs.ThronDockerLambda.addLegacyEndpointAlb">AddLegacyEndpointAlb</a></code> | Add a legacy endpoint to the lambda function. |

---

##### `ToString` <a name="ToString" id="cdk-constructs.ThronDockerLambda.toString"></a>

```go
func ToString() *string
```

Returns a string representation of this construct.

##### `ApplyRemovalPolicy` <a name="ApplyRemovalPolicy" id="cdk-constructs.ThronDockerLambda.applyRemovalPolicy"></a>

```go
func ApplyRemovalPolicy(policy RemovalPolicy)
```

Apply the given removal policy to this resource.

The Removal Policy controls what happens to this resource when it stops
being managed by CloudFormation, either because you've removed it from the
CDK application or because you've made a change that requires the resource
to be replaced.

The resource can be deleted (`RemovalPolicy.DESTROY`), or left in your AWS
account for data recovery and cleanup later (`RemovalPolicy.RETAIN`).

###### `policy`<sup>Required</sup> <a name="policy" id="cdk-constructs.ThronDockerLambda.applyRemovalPolicy.parameter.policy"></a>

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.RemovalPolicy

---

##### `AddEventSource` <a name="AddEventSource" id="cdk-constructs.ThronDockerLambda.addEventSource"></a>

```go
func AddEventSource(source IEventSource)
```

Adds an event source to this function.

Event sources are implemented in the aws-cdk-lib/aws-lambda-event-sources module.

The following example adds an SQS Queue as an event source:
```
import { SqsEventSource } from 'aws-cdk-lib/aws-lambda-event-sources';
myFunction.addEventSource(new SqsEventSource(myQueue));
```

###### `source`<sup>Required</sup> <a name="source" id="cdk-constructs.ThronDockerLambda.addEventSource.parameter.source"></a>

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_lambda.IEventSource

---

##### `AddEventSourceMapping` <a name="AddEventSourceMapping" id="cdk-constructs.ThronDockerLambda.addEventSourceMapping"></a>

```go
func AddEventSourceMapping(id *string, options EventSourceMappingOptions) EventSourceMapping
```

Adds an event source that maps to this AWS Lambda function.

###### `id`<sup>Required</sup> <a name="id" id="cdk-constructs.ThronDockerLambda.addEventSourceMapping.parameter.id"></a>

- *Type:* *string

---

###### `options`<sup>Required</sup> <a name="options" id="cdk-constructs.ThronDockerLambda.addEventSourceMapping.parameter.options"></a>

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_lambda.EventSourceMappingOptions

---

##### `AddFunctionUrl` <a name="AddFunctionUrl" id="cdk-constructs.ThronDockerLambda.addFunctionUrl"></a>

```go
func AddFunctionUrl(options FunctionUrlOptions) FunctionUrl
```

Adds a url to this lambda function.

###### `options`<sup>Optional</sup> <a name="options" id="cdk-constructs.ThronDockerLambda.addFunctionUrl.parameter.options"></a>

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_lambda.FunctionUrlOptions

---

##### `AddPermission` <a name="AddPermission" id="cdk-constructs.ThronDockerLambda.addPermission"></a>

```go
func AddPermission(id *string, permission Permission)
```

Adds a permission to the Lambda resource policy.

> [Permission for details.](Permission for details.)

###### `id`<sup>Required</sup> <a name="id" id="cdk-constructs.ThronDockerLambda.addPermission.parameter.id"></a>

- *Type:* *string

The id for the permission construct.

---

###### `permission`<sup>Required</sup> <a name="permission" id="cdk-constructs.ThronDockerLambda.addPermission.parameter.permission"></a>

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_lambda.Permission

The permission to grant to this Lambda function.

---

##### `AddToRolePolicy` <a name="AddToRolePolicy" id="cdk-constructs.ThronDockerLambda.addToRolePolicy"></a>

```go
func AddToRolePolicy(statement PolicyStatement)
```

Adds a statement to the IAM role assumed by the instance.

###### `statement`<sup>Required</sup> <a name="statement" id="cdk-constructs.ThronDockerLambda.addToRolePolicy.parameter.statement"></a>

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_iam.PolicyStatement

---

##### `ConfigureAsyncInvoke` <a name="ConfigureAsyncInvoke" id="cdk-constructs.ThronDockerLambda.configureAsyncInvoke"></a>

```go
func ConfigureAsyncInvoke(options EventInvokeConfigOptions)
```

Configures options for asynchronous invocation.

###### `options`<sup>Required</sup> <a name="options" id="cdk-constructs.ThronDockerLambda.configureAsyncInvoke.parameter.options"></a>

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_lambda.EventInvokeConfigOptions

---

##### `ConsiderWarningOnInvokeFunctionPermissions` <a name="ConsiderWarningOnInvokeFunctionPermissions" id="cdk-constructs.ThronDockerLambda.considerWarningOnInvokeFunctionPermissions"></a>

```go
func ConsiderWarningOnInvokeFunctionPermissions(scope Construct, action *string)
```

A warning will be added to functions under the following conditions: - permissions that include `lambda:InvokeFunction` are added to the unqualified function.

function.currentVersion is invoked before or after the permission is created.

This applies only to permissions on Lambda functions, not versions or aliases.
This function is overridden as a noOp for QualifiedFunctionBase.

###### `scope`<sup>Required</sup> <a name="scope" id="cdk-constructs.ThronDockerLambda.considerWarningOnInvokeFunctionPermissions.parameter.scope"></a>

- *Type:* github.com/aws/constructs-go/constructs/v10.Construct

---

###### `action`<sup>Required</sup> <a name="action" id="cdk-constructs.ThronDockerLambda.considerWarningOnInvokeFunctionPermissions.parameter.action"></a>

- *Type:* *string

---

##### `GrantInvoke` <a name="GrantInvoke" id="cdk-constructs.ThronDockerLambda.grantInvoke"></a>

```go
func GrantInvoke(grantee IGrantable) Grant
```

Grant the given identity permissions to invoke this Lambda.

###### `grantee`<sup>Required</sup> <a name="grantee" id="cdk-constructs.ThronDockerLambda.grantInvoke.parameter.grantee"></a>

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_iam.IGrantable

---

##### `GrantInvokeCompositePrincipal` <a name="GrantInvokeCompositePrincipal" id="cdk-constructs.ThronDockerLambda.grantInvokeCompositePrincipal"></a>

```go
func GrantInvokeCompositePrincipal(compositePrincipal CompositePrincipal) *[]Grant
```

Grant multiple principals the ability to invoke this Lambda via CompositePrincipal.

###### `compositePrincipal`<sup>Required</sup> <a name="compositePrincipal" id="cdk-constructs.ThronDockerLambda.grantInvokeCompositePrincipal.parameter.compositePrincipal"></a>

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_iam.CompositePrincipal

---

##### `GrantInvokeLatestVersion` <a name="GrantInvokeLatestVersion" id="cdk-constructs.ThronDockerLambda.grantInvokeLatestVersion"></a>

```go
func GrantInvokeLatestVersion(grantee IGrantable) Grant
```

Grant the given identity permissions to invoke the $LATEST version or unqualified version of this Lambda.

###### `grantee`<sup>Required</sup> <a name="grantee" id="cdk-constructs.ThronDockerLambda.grantInvokeLatestVersion.parameter.grantee"></a>

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_iam.IGrantable

---

##### `GrantInvokeUrl` <a name="GrantInvokeUrl" id="cdk-constructs.ThronDockerLambda.grantInvokeUrl"></a>

```go
func GrantInvokeUrl(grantee IGrantable) Grant
```

Grant the given identity permissions to invoke this Lambda Function URL.

###### `grantee`<sup>Required</sup> <a name="grantee" id="cdk-constructs.ThronDockerLambda.grantInvokeUrl.parameter.grantee"></a>

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_iam.IGrantable

---

##### `GrantInvokeVersion` <a name="GrantInvokeVersion" id="cdk-constructs.ThronDockerLambda.grantInvokeVersion"></a>

```go
func GrantInvokeVersion(grantee IGrantable, version IVersion) Grant
```

Grant the given identity permissions to invoke the given version of this Lambda.

###### `grantee`<sup>Required</sup> <a name="grantee" id="cdk-constructs.ThronDockerLambda.grantInvokeVersion.parameter.grantee"></a>

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_iam.IGrantable

---

###### `version`<sup>Required</sup> <a name="version" id="cdk-constructs.ThronDockerLambda.grantInvokeVersion.parameter.version"></a>

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_lambda.IVersion

---

##### `Metric` <a name="Metric" id="cdk-constructs.ThronDockerLambda.metric"></a>

```go
func Metric(metricName *string, props MetricOptions) Metric
```

Return the given named metric for this Function.

###### `metricName`<sup>Required</sup> <a name="metricName" id="cdk-constructs.ThronDockerLambda.metric.parameter.metricName"></a>

- *Type:* *string

---

###### `props`<sup>Optional</sup> <a name="props" id="cdk-constructs.ThronDockerLambda.metric.parameter.props"></a>

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_cloudwatch.MetricOptions

---

##### `MetricDuration` <a name="MetricDuration" id="cdk-constructs.ThronDockerLambda.metricDuration"></a>

```go
func MetricDuration(props MetricOptions) Metric
```

How long execution of this Lambda takes.

Average over 5 minutes

###### `props`<sup>Optional</sup> <a name="props" id="cdk-constructs.ThronDockerLambda.metricDuration.parameter.props"></a>

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_cloudwatch.MetricOptions

---

##### `MetricErrors` <a name="MetricErrors" id="cdk-constructs.ThronDockerLambda.metricErrors"></a>

```go
func MetricErrors(props MetricOptions) Metric
```

How many invocations of this Lambda fail.

Sum over 5 minutes

###### `props`<sup>Optional</sup> <a name="props" id="cdk-constructs.ThronDockerLambda.metricErrors.parameter.props"></a>

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_cloudwatch.MetricOptions

---

##### `MetricInvocations` <a name="MetricInvocations" id="cdk-constructs.ThronDockerLambda.metricInvocations"></a>

```go
func MetricInvocations(props MetricOptions) Metric
```

How often this Lambda is invoked.

Sum over 5 minutes

###### `props`<sup>Optional</sup> <a name="props" id="cdk-constructs.ThronDockerLambda.metricInvocations.parameter.props"></a>

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_cloudwatch.MetricOptions

---

##### `MetricThrottles` <a name="MetricThrottles" id="cdk-constructs.ThronDockerLambda.metricThrottles"></a>

```go
func MetricThrottles(props MetricOptions) Metric
```

How often this Lambda is throttled.

Sum over 5 minutes

###### `props`<sup>Optional</sup> <a name="props" id="cdk-constructs.ThronDockerLambda.metricThrottles.parameter.props"></a>

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_cloudwatch.MetricOptions

---

##### `AddAlias` <a name="AddAlias" id="cdk-constructs.ThronDockerLambda.addAlias"></a>

```go
func AddAlias(aliasName *string, options AliasOptions) Alias
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

- *Type:* *string

The name of the alias.

---

###### `options`<sup>Optional</sup> <a name="options" id="cdk-constructs.ThronDockerLambda.addAlias.parameter.options"></a>

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_lambda.AliasOptions

Alias options.

---

##### `AddEnvironment` <a name="AddEnvironment" id="cdk-constructs.ThronDockerLambda.addEnvironment"></a>

```go
func AddEnvironment(key *string, value *string, options EnvironmentOptions) Function
```

Adds an environment variable to this Lambda function.

If this is a ref to a Lambda function, this operation results in a no-op.

###### `key`<sup>Required</sup> <a name="key" id="cdk-constructs.ThronDockerLambda.addEnvironment.parameter.key"></a>

- *Type:* *string

The environment variable key.

---

###### `value`<sup>Required</sup> <a name="value" id="cdk-constructs.ThronDockerLambda.addEnvironment.parameter.value"></a>

- *Type:* *string

The environment variable's value.

---

###### `options`<sup>Optional</sup> <a name="options" id="cdk-constructs.ThronDockerLambda.addEnvironment.parameter.options"></a>

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_lambda.EnvironmentOptions

Environment variable options.

---

##### `AddLayers` <a name="AddLayers" id="cdk-constructs.ThronDockerLambda.addLayers"></a>

```go
func AddLayers(layers ILayerVersion)
```

Adds one or more Lambda Layers to this Lambda function.

###### `layers`<sup>Required</sup> <a name="layers" id="cdk-constructs.ThronDockerLambda.addLayers.parameter.layers"></a>

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_lambda.ILayerVersion

the layers to be added.

---

##### `InvalidateVersionBasedOn` <a name="InvalidateVersionBasedOn" id="cdk-constructs.ThronDockerLambda.invalidateVersionBasedOn"></a>

```go
func InvalidateVersionBasedOn(x *string)
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

- *Type:* *string

---

##### `AddEndpointAlb` <a name="AddEndpointAlb" id="cdk-constructs.ThronDockerLambda.addEndpointAlb"></a>

```go
func AddEndpointAlb(name *string, endpointProps ThronEndpointAlbProps) EndpointAlb
```

Add an endpoint the lambda function.

###### `name`<sup>Required</sup> <a name="name" id="cdk-constructs.ThronDockerLambda.addEndpointAlb.parameter.name"></a>

- *Type:* *string

---

###### `endpointProps`<sup>Required</sup> <a name="endpointProps" id="cdk-constructs.ThronDockerLambda.addEndpointAlb.parameter.endpointProps"></a>

- *Type:* <a href="#cdk-constructs.ThronEndpointAlbProps">ThronEndpointAlbProps</a>

---

##### `AddLegacyEndpointAlb` <a name="AddLegacyEndpointAlb" id="cdk-constructs.ThronDockerLambda.addLegacyEndpointAlb"></a>

```go
func AddLegacyEndpointAlb(name *string, endpointProps LegacyEndpointAlbProps) EndpointAlb
```

Add a legacy endpoint to the lambda function.

###### `name`<sup>Required</sup> <a name="name" id="cdk-constructs.ThronDockerLambda.addLegacyEndpointAlb.parameter.name"></a>

- *Type:* *string

---

###### `endpointProps`<sup>Required</sup> <a name="endpointProps" id="cdk-constructs.ThronDockerLambda.addLegacyEndpointAlb.parameter.endpointProps"></a>

- *Type:* <a href="#cdk-constructs.LegacyEndpointAlbProps">LegacyEndpointAlbProps</a>

---

#### Static Functions <a name="Static Functions" id="Static Functions"></a>

| **Name** | **Description** |
| --- | --- |
| <code><a href="#cdk-constructs.ThronDockerLambda.isConstruct">IsConstruct</a></code> | Checks if `x` is a construct. |
| <code><a href="#cdk-constructs.ThronDockerLambda.isOwnedResource">IsOwnedResource</a></code> | Returns true if the construct was created by CDK, and false otherwise. |
| <code><a href="#cdk-constructs.ThronDockerLambda.isResource">IsResource</a></code> | Check whether the given construct is a Resource. |
| <code><a href="#cdk-constructs.ThronDockerLambda.classifyVersionProperty">ClassifyVersionProperty</a></code> | Record whether specific properties in the `AWS::Lambda::Function` resource should also be associated to the Version resource. |
| <code><a href="#cdk-constructs.ThronDockerLambda.fromFunctionArn">FromFunctionArn</a></code> | Import a lambda function into the CDK using its ARN. |
| <code><a href="#cdk-constructs.ThronDockerLambda.fromFunctionAttributes">FromFunctionAttributes</a></code> | Creates a Lambda function object which represents a function not defined within this stack. |
| <code><a href="#cdk-constructs.ThronDockerLambda.fromFunctionName">FromFunctionName</a></code> | Import a lambda function into the CDK using its name. |
| <code><a href="#cdk-constructs.ThronDockerLambda.metricAll">MetricAll</a></code> | Return the given named metric for this Lambda. |
| <code><a href="#cdk-constructs.ThronDockerLambda.metricAllConcurrentExecutions">MetricAllConcurrentExecutions</a></code> | Metric for the number of concurrent executions across all Lambdas. |
| <code><a href="#cdk-constructs.ThronDockerLambda.metricAllDuration">MetricAllDuration</a></code> | Metric for the Duration executing all Lambdas. |
| <code><a href="#cdk-constructs.ThronDockerLambda.metricAllErrors">MetricAllErrors</a></code> | Metric for the number of Errors executing all Lambdas. |
| <code><a href="#cdk-constructs.ThronDockerLambda.metricAllInvocations">MetricAllInvocations</a></code> | Metric for the number of invocations of all Lambdas. |
| <code><a href="#cdk-constructs.ThronDockerLambda.metricAllThrottles">MetricAllThrottles</a></code> | Metric for the number of throttled invocations of all Lambdas. |
| <code><a href="#cdk-constructs.ThronDockerLambda.metricAllUnreservedConcurrentExecutions">MetricAllUnreservedConcurrentExecutions</a></code> | Metric for the number of unreserved concurrent executions across all Lambdas. |

---

##### `IsConstruct` <a name="IsConstruct" id="cdk-constructs.ThronDockerLambda.isConstruct"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

cdkconstructs.ThronDockerLambda_IsConstruct(x interface{}) *bool
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

- *Type:* interface{}

Any object.

---

##### `IsOwnedResource` <a name="IsOwnedResource" id="cdk-constructs.ThronDockerLambda.isOwnedResource"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

cdkconstructs.ThronDockerLambda_IsOwnedResource(construct IConstruct) *bool
```

Returns true if the construct was created by CDK, and false otherwise.

###### `construct`<sup>Required</sup> <a name="construct" id="cdk-constructs.ThronDockerLambda.isOwnedResource.parameter.construct"></a>

- *Type:* github.com/aws/constructs-go/constructs/v10.IConstruct

---

##### `IsResource` <a name="IsResource" id="cdk-constructs.ThronDockerLambda.isResource"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

cdkconstructs.ThronDockerLambda_IsResource(construct IConstruct) *bool
```

Check whether the given construct is a Resource.

###### `construct`<sup>Required</sup> <a name="construct" id="cdk-constructs.ThronDockerLambda.isResource.parameter.construct"></a>

- *Type:* github.com/aws/constructs-go/constructs/v10.IConstruct

---

##### `ClassifyVersionProperty` <a name="ClassifyVersionProperty" id="cdk-constructs.ThronDockerLambda.classifyVersionProperty"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

cdkconstructs.ThronDockerLambda_ClassifyVersionProperty(propertyName *string, locked *bool)
```

Record whether specific properties in the `AWS::Lambda::Function` resource should also be associated to the Version resource.

See 'currentVersion' section in the module README for more details.

###### `propertyName`<sup>Required</sup> <a name="propertyName" id="cdk-constructs.ThronDockerLambda.classifyVersionProperty.parameter.propertyName"></a>

- *Type:* *string

The property to classify.

---

###### `locked`<sup>Required</sup> <a name="locked" id="cdk-constructs.ThronDockerLambda.classifyVersionProperty.parameter.locked"></a>

- *Type:* *bool

whether the property should be associated to the version or not.

---

##### `FromFunctionArn` <a name="FromFunctionArn" id="cdk-constructs.ThronDockerLambda.fromFunctionArn"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

cdkconstructs.ThronDockerLambda_FromFunctionArn(scope Construct, id *string, functionArn *string) IFunction
```

Import a lambda function into the CDK using its ARN.

For `Function.addPermissions()` to work on this imported lambda, make sure that is
in the same account and region as the stack you are importing it into.

###### `scope`<sup>Required</sup> <a name="scope" id="cdk-constructs.ThronDockerLambda.fromFunctionArn.parameter.scope"></a>

- *Type:* github.com/aws/constructs-go/constructs/v10.Construct

---

###### `id`<sup>Required</sup> <a name="id" id="cdk-constructs.ThronDockerLambda.fromFunctionArn.parameter.id"></a>

- *Type:* *string

---

###### `functionArn`<sup>Required</sup> <a name="functionArn" id="cdk-constructs.ThronDockerLambda.fromFunctionArn.parameter.functionArn"></a>

- *Type:* *string

---

##### `FromFunctionAttributes` <a name="FromFunctionAttributes" id="cdk-constructs.ThronDockerLambda.fromFunctionAttributes"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

cdkconstructs.ThronDockerLambda_FromFunctionAttributes(scope Construct, id *string, attrs FunctionAttributes) IFunction
```

Creates a Lambda function object which represents a function not defined within this stack.

For `Function.addPermissions()` to work on this imported lambda, set the sameEnvironment property to true
if this imported lambda is in the same account and region as the stack you are importing it into.

###### `scope`<sup>Required</sup> <a name="scope" id="cdk-constructs.ThronDockerLambda.fromFunctionAttributes.parameter.scope"></a>

- *Type:* github.com/aws/constructs-go/constructs/v10.Construct

The parent construct.

---

###### `id`<sup>Required</sup> <a name="id" id="cdk-constructs.ThronDockerLambda.fromFunctionAttributes.parameter.id"></a>

- *Type:* *string

The name of the lambda construct.

---

###### `attrs`<sup>Required</sup> <a name="attrs" id="cdk-constructs.ThronDockerLambda.fromFunctionAttributes.parameter.attrs"></a>

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_lambda.FunctionAttributes

the attributes of the function to import.

---

##### `FromFunctionName` <a name="FromFunctionName" id="cdk-constructs.ThronDockerLambda.fromFunctionName"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

cdkconstructs.ThronDockerLambda_FromFunctionName(scope Construct, id *string, functionName *string) IFunction
```

Import a lambda function into the CDK using its name.

###### `scope`<sup>Required</sup> <a name="scope" id="cdk-constructs.ThronDockerLambda.fromFunctionName.parameter.scope"></a>

- *Type:* github.com/aws/constructs-go/constructs/v10.Construct

---

###### `id`<sup>Required</sup> <a name="id" id="cdk-constructs.ThronDockerLambda.fromFunctionName.parameter.id"></a>

- *Type:* *string

---

###### `functionName`<sup>Required</sup> <a name="functionName" id="cdk-constructs.ThronDockerLambda.fromFunctionName.parameter.functionName"></a>

- *Type:* *string

---

##### `MetricAll` <a name="MetricAll" id="cdk-constructs.ThronDockerLambda.metricAll"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

cdkconstructs.ThronDockerLambda_MetricAll(metricName *string, props MetricOptions) Metric
```

Return the given named metric for this Lambda.

###### `metricName`<sup>Required</sup> <a name="metricName" id="cdk-constructs.ThronDockerLambda.metricAll.parameter.metricName"></a>

- *Type:* *string

---

###### `props`<sup>Optional</sup> <a name="props" id="cdk-constructs.ThronDockerLambda.metricAll.parameter.props"></a>

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_cloudwatch.MetricOptions

---

##### `MetricAllConcurrentExecutions` <a name="MetricAllConcurrentExecutions" id="cdk-constructs.ThronDockerLambda.metricAllConcurrentExecutions"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

cdkconstructs.ThronDockerLambda_MetricAllConcurrentExecutions(props MetricOptions) Metric
```

Metric for the number of concurrent executions across all Lambdas.

###### `props`<sup>Optional</sup> <a name="props" id="cdk-constructs.ThronDockerLambda.metricAllConcurrentExecutions.parameter.props"></a>

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_cloudwatch.MetricOptions

---

##### `MetricAllDuration` <a name="MetricAllDuration" id="cdk-constructs.ThronDockerLambda.metricAllDuration"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

cdkconstructs.ThronDockerLambda_MetricAllDuration(props MetricOptions) Metric
```

Metric for the Duration executing all Lambdas.

###### `props`<sup>Optional</sup> <a name="props" id="cdk-constructs.ThronDockerLambda.metricAllDuration.parameter.props"></a>

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_cloudwatch.MetricOptions

---

##### `MetricAllErrors` <a name="MetricAllErrors" id="cdk-constructs.ThronDockerLambda.metricAllErrors"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

cdkconstructs.ThronDockerLambda_MetricAllErrors(props MetricOptions) Metric
```

Metric for the number of Errors executing all Lambdas.

###### `props`<sup>Optional</sup> <a name="props" id="cdk-constructs.ThronDockerLambda.metricAllErrors.parameter.props"></a>

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_cloudwatch.MetricOptions

---

##### `MetricAllInvocations` <a name="MetricAllInvocations" id="cdk-constructs.ThronDockerLambda.metricAllInvocations"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

cdkconstructs.ThronDockerLambda_MetricAllInvocations(props MetricOptions) Metric
```

Metric for the number of invocations of all Lambdas.

###### `props`<sup>Optional</sup> <a name="props" id="cdk-constructs.ThronDockerLambda.metricAllInvocations.parameter.props"></a>

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_cloudwatch.MetricOptions

---

##### `MetricAllThrottles` <a name="MetricAllThrottles" id="cdk-constructs.ThronDockerLambda.metricAllThrottles"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

cdkconstructs.ThronDockerLambda_MetricAllThrottles(props MetricOptions) Metric
```

Metric for the number of throttled invocations of all Lambdas.

###### `props`<sup>Optional</sup> <a name="props" id="cdk-constructs.ThronDockerLambda.metricAllThrottles.parameter.props"></a>

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_cloudwatch.MetricOptions

---

##### `MetricAllUnreservedConcurrentExecutions` <a name="MetricAllUnreservedConcurrentExecutions" id="cdk-constructs.ThronDockerLambda.metricAllUnreservedConcurrentExecutions"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

cdkconstructs.ThronDockerLambda_MetricAllUnreservedConcurrentExecutions(props MetricOptions) Metric
```

Metric for the number of unreserved concurrent executions across all Lambdas.

###### `props`<sup>Optional</sup> <a name="props" id="cdk-constructs.ThronDockerLambda.metricAllUnreservedConcurrentExecutions.parameter.props"></a>

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_cloudwatch.MetricOptions

---

#### Properties <a name="Properties" id="Properties"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.ThronDockerLambda.property.node">Node</a></code> | <code>github.com/aws/constructs-go/constructs/v10.Node</code> | The tree node. |
| <code><a href="#cdk-constructs.ThronDockerLambda.property.env">Env</a></code> | <code>github.com/aws/aws-cdk-go/awscdk/v2.ResourceEnvironment</code> | The environment this resource belongs to. |
| <code><a href="#cdk-constructs.ThronDockerLambda.property.stack">Stack</a></code> | <code>github.com/aws/aws-cdk-go/awscdk/v2.Stack</code> | The stack in which this resource is defined. |
| <code><a href="#cdk-constructs.ThronDockerLambda.property.architecture">Architecture</a></code> | <code>github.com/aws/aws-cdk-go/awscdk/v2.aws_lambda.Architecture</code> | The architecture of this Lambda Function (this is an optional attribute and defaults to X86_64). |
| <code><a href="#cdk-constructs.ThronDockerLambda.property.connections">Connections</a></code> | <code>github.com/aws/aws-cdk-go/awscdk/v2.aws_ec2.Connections</code> | Access the Connections object. |
| <code><a href="#cdk-constructs.ThronDockerLambda.property.functionArn">FunctionArn</a></code> | <code>*string</code> | ARN of this function. |
| <code><a href="#cdk-constructs.ThronDockerLambda.property.functionName">FunctionName</a></code> | <code>*string</code> | Name of this function. |
| <code><a href="#cdk-constructs.ThronDockerLambda.property.grantPrincipal">GrantPrincipal</a></code> | <code>github.com/aws/aws-cdk-go/awscdk/v2.aws_iam.IPrincipal</code> | The principal this Lambda Function is running as. |
| <code><a href="#cdk-constructs.ThronDockerLambda.property.isBoundToVpc">IsBoundToVpc</a></code> | <code>*bool</code> | Whether or not this Lambda function was bound to a VPC. |
| <code><a href="#cdk-constructs.ThronDockerLambda.property.latestVersion">LatestVersion</a></code> | <code>github.com/aws/aws-cdk-go/awscdk/v2.aws_lambda.IVersion</code> | The `$LATEST` version of this function. |
| <code><a href="#cdk-constructs.ThronDockerLambda.property.permissionsNode">PermissionsNode</a></code> | <code>github.com/aws/constructs-go/constructs/v10.Node</code> | The construct node where permissions are attached. |
| <code><a href="#cdk-constructs.ThronDockerLambda.property.resourceArnsForGrantInvoke">ResourceArnsForGrantInvoke</a></code> | <code>*[]*string</code> | The ARN(s) to put into the resource field of the generated IAM policy for grantInvoke(). |
| <code><a href="#cdk-constructs.ThronDockerLambda.property.role">Role</a></code> | <code>github.com/aws/aws-cdk-go/awscdk/v2.aws_iam.IRole</code> | Execution role associated with this function. |
| <code><a href="#cdk-constructs.ThronDockerLambda.property.currentVersion">CurrentVersion</a></code> | <code>github.com/aws/aws-cdk-go/awscdk/v2.aws_lambda.Version</code> | Returns a `lambda.Version` which represents the current version of this Lambda function. A new version will be created every time the function's configuration changes. |
| <code><a href="#cdk-constructs.ThronDockerLambda.property.logGroup">LogGroup</a></code> | <code>github.com/aws/aws-cdk-go/awscdk/v2.aws_logs.ILogGroup</code> | The LogGroup where the Lambda function's logs are made available. |
| <code><a href="#cdk-constructs.ThronDockerLambda.property.runtime">Runtime</a></code> | <code>github.com/aws/aws-cdk-go/awscdk/v2.aws_lambda.Runtime</code> | The runtime configured for this lambda. |
| <code><a href="#cdk-constructs.ThronDockerLambda.property.deadLetterQueue">DeadLetterQueue</a></code> | <code>github.com/aws/aws-cdk-go/awscdk/v2.aws_sqs.IQueue</code> | The DLQ (as queue) associated with this Lambda Function (this is an optional attribute). |
| <code><a href="#cdk-constructs.ThronDockerLambda.property.deadLetterTopic">DeadLetterTopic</a></code> | <code>github.com/aws/aws-cdk-go/awscdk/v2.aws_sns.ITopic</code> | The DLQ (as topic) associated with this Lambda Function (this is an optional attribute). |
| <code><a href="#cdk-constructs.ThronDockerLambda.property.timeout">Timeout</a></code> | <code>github.com/aws/aws-cdk-go/awscdk/v2.Duration</code> | The timeout configured for this lambda. |
| <code><a href="#cdk-constructs.ThronDockerLambda.property.apiGatewayEndpoints">ApiGatewayEndpoints</a></code> | <code>*map[string]<a href="#cdk-constructs.ThronCreatedApiGatewayEndpoint">ThronCreatedApiGatewayEndpoint</a></code> | *No description.* |
| <code><a href="#cdk-constructs.ThronDockerLambda.property.endpoints">Endpoints</a></code> | <code>*map[string]<a href="#cdk-constructs.EndpointAlb">EndpointAlb</a></code> | *No description.* |
| <code><a href="#cdk-constructs.ThronDockerLambda.property.legacyEndpoints">LegacyEndpoints</a></code> | <code>*map[string]<a href="#cdk-constructs.EndpointAlb">EndpointAlb</a></code> | *No description.* |

---

##### `Node`<sup>Required</sup> <a name="Node" id="cdk-constructs.ThronDockerLambda.property.node"></a>

```go
func Node() Node
```

- *Type:* github.com/aws/constructs-go/constructs/v10.Node

The tree node.

---

##### `Env`<sup>Required</sup> <a name="Env" id="cdk-constructs.ThronDockerLambda.property.env"></a>

```go
func Env() ResourceEnvironment
```

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.ResourceEnvironment

The environment this resource belongs to.

For resources that are created and managed by the CDK
(generally, those created by creating new class instances like Role, Bucket, etc.),
this is always the same as the environment of the stack they belong to;
however, for imported resources
(those obtained from static methods like fromRoleArn, fromBucketName, etc.),
that might be different than the stack they were imported into.

---

##### `Stack`<sup>Required</sup> <a name="Stack" id="cdk-constructs.ThronDockerLambda.property.stack"></a>

```go
func Stack() Stack
```

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.Stack

The stack in which this resource is defined.

---

##### `Architecture`<sup>Required</sup> <a name="Architecture" id="cdk-constructs.ThronDockerLambda.property.architecture"></a>

```go
func Architecture() Architecture
```

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_lambda.Architecture

The architecture of this Lambda Function (this is an optional attribute and defaults to X86_64).

---

##### `Connections`<sup>Required</sup> <a name="Connections" id="cdk-constructs.ThronDockerLambda.property.connections"></a>

```go
func Connections() Connections
```

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_ec2.Connections

Access the Connections object.

Will fail if not a VPC-enabled Lambda Function

---

##### `FunctionArn`<sup>Required</sup> <a name="FunctionArn" id="cdk-constructs.ThronDockerLambda.property.functionArn"></a>

```go
func FunctionArn() *string
```

- *Type:* *string

ARN of this function.

---

##### `FunctionName`<sup>Required</sup> <a name="FunctionName" id="cdk-constructs.ThronDockerLambda.property.functionName"></a>

```go
func FunctionName() *string
```

- *Type:* *string

Name of this function.

---

##### `GrantPrincipal`<sup>Required</sup> <a name="GrantPrincipal" id="cdk-constructs.ThronDockerLambda.property.grantPrincipal"></a>

```go
func GrantPrincipal() IPrincipal
```

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_iam.IPrincipal

The principal this Lambda Function is running as.

---

##### `IsBoundToVpc`<sup>Required</sup> <a name="IsBoundToVpc" id="cdk-constructs.ThronDockerLambda.property.isBoundToVpc"></a>

```go
func IsBoundToVpc() *bool
```

- *Type:* *bool

Whether or not this Lambda function was bound to a VPC.

If this is is `false`, trying to access the `connections` object will fail.

---

##### `LatestVersion`<sup>Required</sup> <a name="LatestVersion" id="cdk-constructs.ThronDockerLambda.property.latestVersion"></a>

```go
func LatestVersion() IVersion
```

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_lambda.IVersion

The `$LATEST` version of this function.

Note that this is reference to a non-specific AWS Lambda version, which
means the function this version refers to can return different results in
different invocations.

To obtain a reference to an explicit version which references the current
function configuration, use `lambdaFunction.currentVersion` instead.

---

##### `PermissionsNode`<sup>Required</sup> <a name="PermissionsNode" id="cdk-constructs.ThronDockerLambda.property.permissionsNode"></a>

```go
func PermissionsNode() Node
```

- *Type:* github.com/aws/constructs-go/constructs/v10.Node

The construct node where permissions are attached.

---

##### `ResourceArnsForGrantInvoke`<sup>Required</sup> <a name="ResourceArnsForGrantInvoke" id="cdk-constructs.ThronDockerLambda.property.resourceArnsForGrantInvoke"></a>

```go
func ResourceArnsForGrantInvoke() *[]*string
```

- *Type:* *[]*string

The ARN(s) to put into the resource field of the generated IAM policy for grantInvoke().

---

##### `Role`<sup>Optional</sup> <a name="Role" id="cdk-constructs.ThronDockerLambda.property.role"></a>

```go
func Role() IRole
```

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_iam.IRole

Execution role associated with this function.

---

##### `CurrentVersion`<sup>Required</sup> <a name="CurrentVersion" id="cdk-constructs.ThronDockerLambda.property.currentVersion"></a>

```go
func CurrentVersion() Version
```

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_lambda.Version

Returns a `lambda.Version` which represents the current version of this Lambda function. A new version will be created every time the function's configuration changes.

You can specify options for this version using the `currentVersionOptions`
prop when initializing the `lambda.Function`.

---

##### `LogGroup`<sup>Required</sup> <a name="LogGroup" id="cdk-constructs.ThronDockerLambda.property.logGroup"></a>

```go
func LogGroup() ILogGroup
```

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_logs.ILogGroup

The LogGroup where the Lambda function's logs are made available.

If either `logRetention` is set or this property is called, a CloudFormation custom resource is added to the stack that
pre-creates the log group as part of the stack deployment, if it already doesn't exist, and sets the correct log retention
period (never expire, by default).

Further, if the log group already exists and the `logRetention` is not set, the custom resource will reset the log retention
to never expire even if it was configured with a different value.

---

##### `Runtime`<sup>Required</sup> <a name="Runtime" id="cdk-constructs.ThronDockerLambda.property.runtime"></a>

```go
func Runtime() Runtime
```

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_lambda.Runtime

The runtime configured for this lambda.

---

##### `DeadLetterQueue`<sup>Optional</sup> <a name="DeadLetterQueue" id="cdk-constructs.ThronDockerLambda.property.deadLetterQueue"></a>

```go
func DeadLetterQueue() IQueue
```

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_sqs.IQueue

The DLQ (as queue) associated with this Lambda Function (this is an optional attribute).

---

##### `DeadLetterTopic`<sup>Optional</sup> <a name="DeadLetterTopic" id="cdk-constructs.ThronDockerLambda.property.deadLetterTopic"></a>

```go
func DeadLetterTopic() ITopic
```

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_sns.ITopic

The DLQ (as topic) associated with this Lambda Function (this is an optional attribute).

---

##### `Timeout`<sup>Optional</sup> <a name="Timeout" id="cdk-constructs.ThronDockerLambda.property.timeout"></a>

```go
func Timeout() Duration
```

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.Duration

The timeout configured for this lambda.

---

##### `ApiGatewayEndpoints`<sup>Optional</sup> <a name="ApiGatewayEndpoints" id="cdk-constructs.ThronDockerLambda.property.apiGatewayEndpoints"></a>

```go
func ApiGatewayEndpoints() *map[string]ThronCreatedApiGatewayEndpoint
```

- *Type:* *map[string]<a href="#cdk-constructs.ThronCreatedApiGatewayEndpoint">ThronCreatedApiGatewayEndpoint</a>

---

##### `Endpoints`<sup>Optional</sup> <a name="Endpoints" id="cdk-constructs.ThronDockerLambda.property.endpoints"></a>

```go
func Endpoints() *map[string]EndpointAlb
```

- *Type:* *map[string]<a href="#cdk-constructs.EndpointAlb">EndpointAlb</a>

---

##### `LegacyEndpoints`<sup>Optional</sup> <a name="LegacyEndpoints" id="cdk-constructs.ThronDockerLambda.property.legacyEndpoints"></a>

```go
func LegacyEndpoints() *map[string]EndpointAlb
```

- *Type:* *map[string]<a href="#cdk-constructs.EndpointAlb">EndpointAlb</a>

---


### ThronEc2Service <a name="ThronEc2Service" id="cdk-constructs.ThronEc2Service"></a>

#### Initializers <a name="Initializers" id="cdk-constructs.ThronEc2Service.Initializer"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

cdkconstructs.NewThronEc2Service(scope Stack, id *string, props ThronEc2ServiceProps) ThronEc2Service
```

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.ThronEc2Service.Initializer.parameter.scope">scope</a></code> | <code>github.com/aws/aws-cdk-go/awscdk/v2.Stack</code> | *No description.* |
| <code><a href="#cdk-constructs.ThronEc2Service.Initializer.parameter.id">id</a></code> | <code>*string</code> | *No description.* |
| <code><a href="#cdk-constructs.ThronEc2Service.Initializer.parameter.props">props</a></code> | <code><a href="#cdk-constructs.ThronEc2ServiceProps">ThronEc2ServiceProps</a></code> | *No description.* |

---

##### `scope`<sup>Required</sup> <a name="scope" id="cdk-constructs.ThronEc2Service.Initializer.parameter.scope"></a>

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.Stack

---

##### `id`<sup>Required</sup> <a name="id" id="cdk-constructs.ThronEc2Service.Initializer.parameter.id"></a>

- *Type:* *string

---

##### `props`<sup>Required</sup> <a name="props" id="cdk-constructs.ThronEc2Service.Initializer.parameter.props"></a>

- *Type:* <a href="#cdk-constructs.ThronEc2ServiceProps">ThronEc2ServiceProps</a>

---

#### Methods <a name="Methods" id="Methods"></a>

| **Name** | **Description** |
| --- | --- |
| <code><a href="#cdk-constructs.ThronEc2Service.toString">ToString</a></code> | Returns a string representation of this construct. |
| <code><a href="#cdk-constructs.ThronEc2Service.applyRemovalPolicy">ApplyRemovalPolicy</a></code> | Apply the given removal policy to this resource. |
| <code><a href="#cdk-constructs.ThronEc2Service.addVolume">AddVolume</a></code> | Adds a volume to the Service. |
| <code><a href="#cdk-constructs.ThronEc2Service.associateCloudMapService">AssociateCloudMapService</a></code> | Associates this service with a CloudMap service. |
| <code><a href="#cdk-constructs.ThronEc2Service.attachToApplicationTargetGroup">AttachToApplicationTargetGroup</a></code> | This method is called to attach this service to an Application Load Balancer. |
| <code><a href="#cdk-constructs.ThronEc2Service.attachToClassicLB">AttachToClassicLB</a></code> | Registers the service as a target of a Classic Load Balancer (CLB). |
| <code><a href="#cdk-constructs.ThronEc2Service.attachToNetworkTargetGroup">AttachToNetworkTargetGroup</a></code> | This method is called to attach this service to a Network Load Balancer. |
| <code><a href="#cdk-constructs.ThronEc2Service.autoScaleTaskCount">AutoScaleTaskCount</a></code> | An attribute representing the minimum and maximum task count for an AutoScalingGroup. |
| <code><a href="#cdk-constructs.ThronEc2Service.enableCloudMap">EnableCloudMap</a></code> | Enable CloudMap service discovery for the service. |
| <code><a href="#cdk-constructs.ThronEc2Service.enableDeploymentAlarms">EnableDeploymentAlarms</a></code> | Enable Deployment Alarms which take advantage of arbitrary alarms and configure them after service initialization. |
| <code><a href="#cdk-constructs.ThronEc2Service.enableServiceConnect">EnableServiceConnect</a></code> | Enable Service Connect on this service. |
| <code><a href="#cdk-constructs.ThronEc2Service.loadBalancerTarget">LoadBalancerTarget</a></code> | Return a load balancing target for a specific container and port. |
| <code><a href="#cdk-constructs.ThronEc2Service.metric">Metric</a></code> | This method returns the specified CloudWatch metric name for this service. |
| <code><a href="#cdk-constructs.ThronEc2Service.metricCpuUtilization">MetricCpuUtilization</a></code> | This method returns the CloudWatch metric for this service's CPU utilization. |
| <code><a href="#cdk-constructs.ThronEc2Service.metricMemoryUtilization">MetricMemoryUtilization</a></code> | This method returns the CloudWatch metric for this service's memory utilization. |
| <code><a href="#cdk-constructs.ThronEc2Service.registerLoadBalancerTargets">RegisterLoadBalancerTargets</a></code> | Use this function to create all load balancer targets to be registered in this service, add them to target groups, and attach target groups to listeners accordingly. |
| <code><a href="#cdk-constructs.ThronEc2Service.addPlacementConstraints">AddPlacementConstraints</a></code> | Adds one or more placement constraints to use for tasks in the service. |
| <code><a href="#cdk-constructs.ThronEc2Service.addPlacementStrategies">AddPlacementStrategies</a></code> | Adds one or more placement strategies to use for tasks in the service. |
| <code><a href="#cdk-constructs.ThronEc2Service.addEndpointAlb">AddEndpointAlb</a></code> | Add an endpoint for the EC2 service. |
| <code><a href="#cdk-constructs.ThronEc2Service.addLegacyEndpointAlb">AddLegacyEndpointAlb</a></code> | Add a legacy endpoint for the EC2 service. |
| <code><a href="#cdk-constructs.ThronEc2Service.addTargetScaling">AddTargetScaling</a></code> | Configures an EC2 service as a scalable target. |

---

##### `ToString` <a name="ToString" id="cdk-constructs.ThronEc2Service.toString"></a>

```go
func ToString() *string
```

Returns a string representation of this construct.

##### `ApplyRemovalPolicy` <a name="ApplyRemovalPolicy" id="cdk-constructs.ThronEc2Service.applyRemovalPolicy"></a>

```go
func ApplyRemovalPolicy(policy RemovalPolicy)
```

Apply the given removal policy to this resource.

The Removal Policy controls what happens to this resource when it stops
being managed by CloudFormation, either because you've removed it from the
CDK application or because you've made a change that requires the resource
to be replaced.

The resource can be deleted (`RemovalPolicy.DESTROY`), or left in your AWS
account for data recovery and cleanup later (`RemovalPolicy.RETAIN`).

###### `policy`<sup>Required</sup> <a name="policy" id="cdk-constructs.ThronEc2Service.applyRemovalPolicy.parameter.policy"></a>

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.RemovalPolicy

---

##### `AddVolume` <a name="AddVolume" id="cdk-constructs.ThronEc2Service.addVolume"></a>

```go
func AddVolume(volume ServiceManagedVolume)
```

Adds a volume to the Service.

###### `volume`<sup>Required</sup> <a name="volume" id="cdk-constructs.ThronEc2Service.addVolume.parameter.volume"></a>

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_ecs.ServiceManagedVolume

---

##### `AssociateCloudMapService` <a name="AssociateCloudMapService" id="cdk-constructs.ThronEc2Service.associateCloudMapService"></a>

```go
func AssociateCloudMapService(options AssociateCloudMapServiceOptions)
```

Associates this service with a CloudMap service.

###### `options`<sup>Required</sup> <a name="options" id="cdk-constructs.ThronEc2Service.associateCloudMapService.parameter.options"></a>

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_ecs.AssociateCloudMapServiceOptions

---

##### `AttachToApplicationTargetGroup` <a name="AttachToApplicationTargetGroup" id="cdk-constructs.ThronEc2Service.attachToApplicationTargetGroup"></a>

```go
func AttachToApplicationTargetGroup(targetGroup IApplicationTargetGroup) LoadBalancerTargetProps
```

This method is called to attach this service to an Application Load Balancer.

Don't call this function directly. Instead, call `listener.addTargets()`
to add this service to a load balancer.

###### `targetGroup`<sup>Required</sup> <a name="targetGroup" id="cdk-constructs.ThronEc2Service.attachToApplicationTargetGroup.parameter.targetGroup"></a>

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_elasticloadbalancingv2.IApplicationTargetGroup

---

##### `AttachToClassicLB` <a name="AttachToClassicLB" id="cdk-constructs.ThronEc2Service.attachToClassicLB"></a>

```go
func AttachToClassicLB(loadBalancer LoadBalancer)
```

Registers the service as a target of a Classic Load Balancer (CLB).

Don't call this. Call `loadBalancer.addTarget()` instead.

###### `loadBalancer`<sup>Required</sup> <a name="loadBalancer" id="cdk-constructs.ThronEc2Service.attachToClassicLB.parameter.loadBalancer"></a>

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_elasticloadbalancing.LoadBalancer

---

##### `AttachToNetworkTargetGroup` <a name="AttachToNetworkTargetGroup" id="cdk-constructs.ThronEc2Service.attachToNetworkTargetGroup"></a>

```go
func AttachToNetworkTargetGroup(targetGroup INetworkTargetGroup) LoadBalancerTargetProps
```

This method is called to attach this service to a Network Load Balancer.

Don't call this function directly. Instead, call `listener.addTargets()`
to add this service to a load balancer.

###### `targetGroup`<sup>Required</sup> <a name="targetGroup" id="cdk-constructs.ThronEc2Service.attachToNetworkTargetGroup.parameter.targetGroup"></a>

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_elasticloadbalancingv2.INetworkTargetGroup

---

##### `AutoScaleTaskCount` <a name="AutoScaleTaskCount" id="cdk-constructs.ThronEc2Service.autoScaleTaskCount"></a>

```go
func AutoScaleTaskCount(props EnableScalingProps) ScalableTaskCount
```

An attribute representing the minimum and maximum task count for an AutoScalingGroup.

###### `props`<sup>Required</sup> <a name="props" id="cdk-constructs.ThronEc2Service.autoScaleTaskCount.parameter.props"></a>

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_applicationautoscaling.EnableScalingProps

---

##### `EnableCloudMap` <a name="EnableCloudMap" id="cdk-constructs.ThronEc2Service.enableCloudMap"></a>

```go
func EnableCloudMap(options CloudMapOptions) Service
```

Enable CloudMap service discovery for the service.

###### `options`<sup>Required</sup> <a name="options" id="cdk-constructs.ThronEc2Service.enableCloudMap.parameter.options"></a>

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_ecs.CloudMapOptions

---

##### `EnableDeploymentAlarms` <a name="EnableDeploymentAlarms" id="cdk-constructs.ThronEc2Service.enableDeploymentAlarms"></a>

```go
func EnableDeploymentAlarms(alarmNames *[]*string, options DeploymentAlarmOptions)
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

- *Type:* *[]*string

---

###### `options`<sup>Optional</sup> <a name="options" id="cdk-constructs.ThronEc2Service.enableDeploymentAlarms.parameter.options"></a>

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_ecs.DeploymentAlarmOptions

---

##### `EnableServiceConnect` <a name="EnableServiceConnect" id="cdk-constructs.ThronEc2Service.enableServiceConnect"></a>

```go
func EnableServiceConnect(config ServiceConnectProps)
```

Enable Service Connect on this service.

###### `config`<sup>Optional</sup> <a name="config" id="cdk-constructs.ThronEc2Service.enableServiceConnect.parameter.config"></a>

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_ecs.ServiceConnectProps

---

##### `LoadBalancerTarget` <a name="LoadBalancerTarget" id="cdk-constructs.ThronEc2Service.loadBalancerTarget"></a>

```go
func LoadBalancerTarget(options LoadBalancerTargetOptions) IEcsLoadBalancerTarget
```

Return a load balancing target for a specific container and port.

Use this function to create a load balancer target if you want to load balance to
another container than the first essential container or the first mapped port on
the container.

Use the return value of this function where you would normally use a load balancer
target, instead of the `Service` object itself.

*Example*

```go
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

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_ecs.LoadBalancerTargetOptions

---

##### `Metric` <a name="Metric" id="cdk-constructs.ThronEc2Service.metric"></a>

```go
func Metric(metricName *string, props MetricOptions) Metric
```

This method returns the specified CloudWatch metric name for this service.

###### `metricName`<sup>Required</sup> <a name="metricName" id="cdk-constructs.ThronEc2Service.metric.parameter.metricName"></a>

- *Type:* *string

---

###### `props`<sup>Optional</sup> <a name="props" id="cdk-constructs.ThronEc2Service.metric.parameter.props"></a>

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_cloudwatch.MetricOptions

---

##### `MetricCpuUtilization` <a name="MetricCpuUtilization" id="cdk-constructs.ThronEc2Service.metricCpuUtilization"></a>

```go
func MetricCpuUtilization(props MetricOptions) Metric
```

This method returns the CloudWatch metric for this service's CPU utilization.

###### `props`<sup>Optional</sup> <a name="props" id="cdk-constructs.ThronEc2Service.metricCpuUtilization.parameter.props"></a>

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_cloudwatch.MetricOptions

---

##### `MetricMemoryUtilization` <a name="MetricMemoryUtilization" id="cdk-constructs.ThronEc2Service.metricMemoryUtilization"></a>

```go
func MetricMemoryUtilization(props MetricOptions) Metric
```

This method returns the CloudWatch metric for this service's memory utilization.

###### `props`<sup>Optional</sup> <a name="props" id="cdk-constructs.ThronEc2Service.metricMemoryUtilization.parameter.props"></a>

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_cloudwatch.MetricOptions

---

##### `RegisterLoadBalancerTargets` <a name="RegisterLoadBalancerTargets" id="cdk-constructs.ThronEc2Service.registerLoadBalancerTargets"></a>

```go
func RegisterLoadBalancerTargets(targets EcsTarget)
```

Use this function to create all load balancer targets to be registered in this service, add them to target groups, and attach target groups to listeners accordingly.

Alternatively, you can use `listener.addTargets()` to create targets and add them to target groups.

*Example*

```go
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

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_ecs.EcsTarget

---

##### `AddPlacementConstraints` <a name="AddPlacementConstraints" id="cdk-constructs.ThronEc2Service.addPlacementConstraints"></a>

```go
func AddPlacementConstraints(constraints PlacementConstraint)
```

Adds one or more placement constraints to use for tasks in the service.

For more information, see
[Amazon ECS Task Placement Constraints](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/task-placement-constraints.html).

###### `constraints`<sup>Required</sup> <a name="constraints" id="cdk-constructs.ThronEc2Service.addPlacementConstraints.parameter.constraints"></a>

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_ecs.PlacementConstraint

---

##### `AddPlacementStrategies` <a name="AddPlacementStrategies" id="cdk-constructs.ThronEc2Service.addPlacementStrategies"></a>

```go
func AddPlacementStrategies(strategies PlacementStrategy)
```

Adds one or more placement strategies to use for tasks in the service.

For more information, see
[Amazon ECS Task Placement Strategies](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/task-placement-strategies.html).

###### `strategies`<sup>Required</sup> <a name="strategies" id="cdk-constructs.ThronEc2Service.addPlacementStrategies.parameter.strategies"></a>

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_ecs.PlacementStrategy

---

##### `AddEndpointAlb` <a name="AddEndpointAlb" id="cdk-constructs.ThronEc2Service.addEndpointAlb"></a>

```go
func AddEndpointAlb(name *string, endpointProps ThronEndpointAlbProps) EndpointAlb
```

Add an endpoint for the EC2 service.

###### `name`<sup>Required</sup> <a name="name" id="cdk-constructs.ThronEc2Service.addEndpointAlb.parameter.name"></a>

- *Type:* *string

---

###### `endpointProps`<sup>Required</sup> <a name="endpointProps" id="cdk-constructs.ThronEc2Service.addEndpointAlb.parameter.endpointProps"></a>

- *Type:* <a href="#cdk-constructs.ThronEndpointAlbProps">ThronEndpointAlbProps</a>

---

##### `AddLegacyEndpointAlb` <a name="AddLegacyEndpointAlb" id="cdk-constructs.ThronEc2Service.addLegacyEndpointAlb"></a>

```go
func AddLegacyEndpointAlb(name *string, endpointProps LegacyEndpointAlbProps) EndpointAlb
```

Add a legacy endpoint for the EC2 service.

###### `name`<sup>Required</sup> <a name="name" id="cdk-constructs.ThronEc2Service.addLegacyEndpointAlb.parameter.name"></a>

- *Type:* *string

---

###### `endpointProps`<sup>Required</sup> <a name="endpointProps" id="cdk-constructs.ThronEc2Service.addLegacyEndpointAlb.parameter.endpointProps"></a>

- *Type:* <a href="#cdk-constructs.LegacyEndpointAlbProps">LegacyEndpointAlbProps</a>

---

##### `AddTargetScaling` <a name="AddTargetScaling" id="cdk-constructs.ThronEc2Service.addTargetScaling"></a>

```go
func AddTargetScaling(targetScaling ThronTargetScalingProps) ThronEc2TargetScaling
```

Configures an EC2 service as a scalable target.

###### `targetScaling`<sup>Required</sup> <a name="targetScaling" id="cdk-constructs.ThronEc2Service.addTargetScaling.parameter.targetScaling"></a>

- *Type:* <a href="#cdk-constructs.ThronTargetScalingProps">ThronTargetScalingProps</a>

target scaling property.

---

#### Static Functions <a name="Static Functions" id="Static Functions"></a>

| **Name** | **Description** |
| --- | --- |
| <code><a href="#cdk-constructs.ThronEc2Service.isConstruct">IsConstruct</a></code> | Checks if `x` is a construct. |
| <code><a href="#cdk-constructs.ThronEc2Service.isOwnedResource">IsOwnedResource</a></code> | Returns true if the construct was created by CDK, and false otherwise. |
| <code><a href="#cdk-constructs.ThronEc2Service.isResource">IsResource</a></code> | Check whether the given construct is a Resource. |
| <code><a href="#cdk-constructs.ThronEc2Service.fromServiceArnWithCluster">FromServiceArnWithCluster</a></code> | Import an existing ECS/Fargate Service using the service cluster format. |
| <code><a href="#cdk-constructs.ThronEc2Service.fromEc2ServiceArn">FromEc2ServiceArn</a></code> | Imports from the specified service ARN. |
| <code><a href="#cdk-constructs.ThronEc2Service.fromEc2ServiceAttributes">FromEc2ServiceAttributes</a></code> | Imports from the specified service attributes. |

---

##### `IsConstruct` <a name="IsConstruct" id="cdk-constructs.ThronEc2Service.isConstruct"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

cdkconstructs.ThronEc2Service_IsConstruct(x interface{}) *bool
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

- *Type:* interface{}

Any object.

---

##### `IsOwnedResource` <a name="IsOwnedResource" id="cdk-constructs.ThronEc2Service.isOwnedResource"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

cdkconstructs.ThronEc2Service_IsOwnedResource(construct IConstruct) *bool
```

Returns true if the construct was created by CDK, and false otherwise.

###### `construct`<sup>Required</sup> <a name="construct" id="cdk-constructs.ThronEc2Service.isOwnedResource.parameter.construct"></a>

- *Type:* github.com/aws/constructs-go/constructs/v10.IConstruct

---

##### `IsResource` <a name="IsResource" id="cdk-constructs.ThronEc2Service.isResource"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

cdkconstructs.ThronEc2Service_IsResource(construct IConstruct) *bool
```

Check whether the given construct is a Resource.

###### `construct`<sup>Required</sup> <a name="construct" id="cdk-constructs.ThronEc2Service.isResource.parameter.construct"></a>

- *Type:* github.com/aws/constructs-go/constructs/v10.IConstruct

---

##### `FromServiceArnWithCluster` <a name="FromServiceArnWithCluster" id="cdk-constructs.ThronEc2Service.fromServiceArnWithCluster"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

cdkconstructs.ThronEc2Service_FromServiceArnWithCluster(scope Construct, id *string, serviceArn *string) IBaseService
```

Import an existing ECS/Fargate Service using the service cluster format.

The format is the "new" format "arn:aws:ecs:region:aws_account_id:service/cluster-name/service-name".

> [https://docs.aws.amazon.com/AmazonECS/latest/developerguide/ecs-account-settings.html#ecs-resource-ids](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/ecs-account-settings.html#ecs-resource-ids)

###### `scope`<sup>Required</sup> <a name="scope" id="cdk-constructs.ThronEc2Service.fromServiceArnWithCluster.parameter.scope"></a>

- *Type:* github.com/aws/constructs-go/constructs/v10.Construct

---

###### `id`<sup>Required</sup> <a name="id" id="cdk-constructs.ThronEc2Service.fromServiceArnWithCluster.parameter.id"></a>

- *Type:* *string

---

###### `serviceArn`<sup>Required</sup> <a name="serviceArn" id="cdk-constructs.ThronEc2Service.fromServiceArnWithCluster.parameter.serviceArn"></a>

- *Type:* *string

---

##### `FromEc2ServiceArn` <a name="FromEc2ServiceArn" id="cdk-constructs.ThronEc2Service.fromEc2ServiceArn"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

cdkconstructs.ThronEc2Service_FromEc2ServiceArn(scope Construct, id *string, ec2ServiceArn *string) IEc2Service
```

Imports from the specified service ARN.

###### `scope`<sup>Required</sup> <a name="scope" id="cdk-constructs.ThronEc2Service.fromEc2ServiceArn.parameter.scope"></a>

- *Type:* github.com/aws/constructs-go/constructs/v10.Construct

---

###### `id`<sup>Required</sup> <a name="id" id="cdk-constructs.ThronEc2Service.fromEc2ServiceArn.parameter.id"></a>

- *Type:* *string

---

###### `ec2ServiceArn`<sup>Required</sup> <a name="ec2ServiceArn" id="cdk-constructs.ThronEc2Service.fromEc2ServiceArn.parameter.ec2ServiceArn"></a>

- *Type:* *string

---

##### `FromEc2ServiceAttributes` <a name="FromEc2ServiceAttributes" id="cdk-constructs.ThronEc2Service.fromEc2ServiceAttributes"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

cdkconstructs.ThronEc2Service_FromEc2ServiceAttributes(scope Construct, id *string, attrs Ec2ServiceAttributes) IBaseService
```

Imports from the specified service attributes.

###### `scope`<sup>Required</sup> <a name="scope" id="cdk-constructs.ThronEc2Service.fromEc2ServiceAttributes.parameter.scope"></a>

- *Type:* github.com/aws/constructs-go/constructs/v10.Construct

---

###### `id`<sup>Required</sup> <a name="id" id="cdk-constructs.ThronEc2Service.fromEc2ServiceAttributes.parameter.id"></a>

- *Type:* *string

---

###### `attrs`<sup>Required</sup> <a name="attrs" id="cdk-constructs.ThronEc2Service.fromEc2ServiceAttributes.parameter.attrs"></a>

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_ecs.Ec2ServiceAttributes

---

#### Properties <a name="Properties" id="Properties"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.ThronEc2Service.property.node">Node</a></code> | <code>github.com/aws/constructs-go/constructs/v10.Node</code> | The tree node. |
| <code><a href="#cdk-constructs.ThronEc2Service.property.env">Env</a></code> | <code>github.com/aws/aws-cdk-go/awscdk/v2.ResourceEnvironment</code> | The environment this resource belongs to. |
| <code><a href="#cdk-constructs.ThronEc2Service.property.stack">Stack</a></code> | <code>github.com/aws/aws-cdk-go/awscdk/v2.Stack</code> | The stack in which this resource is defined. |
| <code><a href="#cdk-constructs.ThronEc2Service.property.cluster">Cluster</a></code> | <code>github.com/aws/aws-cdk-go/awscdk/v2.aws_ecs.ICluster</code> | The cluster that hosts the service. |
| <code><a href="#cdk-constructs.ThronEc2Service.property.connections">Connections</a></code> | <code>github.com/aws/aws-cdk-go/awscdk/v2.aws_ec2.Connections</code> | The security groups which manage the allowed network traffic for the service. |
| <code><a href="#cdk-constructs.ThronEc2Service.property.serviceArn">ServiceArn</a></code> | <code>*string</code> | The Amazon Resource Name (ARN) of the service. |
| <code><a href="#cdk-constructs.ThronEc2Service.property.serviceName">ServiceName</a></code> | <code>*string</code> | The name of the service. |
| <code><a href="#cdk-constructs.ThronEc2Service.property.taskDefinition">TaskDefinition</a></code> | <code>github.com/aws/aws-cdk-go/awscdk/v2.aws_ecs.TaskDefinition</code> | The task definition to use for tasks in the service. |
| <code><a href="#cdk-constructs.ThronEc2Service.property.cloudMapService">CloudMapService</a></code> | <code>github.com/aws/aws-cdk-go/awscdk/v2.aws_servicediscovery.IService</code> | The CloudMap service created for this service, if any. |
| <code><a href="#cdk-constructs.ThronEc2Service.property.ec2TaskDefinition">Ec2TaskDefinition</a></code> | <code><a href="#cdk-constructs.ThronEc2TaskDefinition">ThronEc2TaskDefinition</a></code> | *No description.* |
| <code><a href="#cdk-constructs.ThronEc2Service.property.endpoints">Endpoints</a></code> | <code>*map[string]<a href="#cdk-constructs.EndpointAlb">EndpointAlb</a></code> | *No description.* |
| <code><a href="#cdk-constructs.ThronEc2Service.property.legacyEndpoints">LegacyEndpoints</a></code> | <code>*map[string]<a href="#cdk-constructs.EndpointAlb">EndpointAlb</a></code> | *No description.* |
| <code><a href="#cdk-constructs.ThronEc2Service.property.targetScaling">TargetScaling</a></code> | <code><a href="#cdk-constructs.ThronTargetScaling">ThronTargetScaling</a></code> | *No description.* |

---

##### `Node`<sup>Required</sup> <a name="Node" id="cdk-constructs.ThronEc2Service.property.node"></a>

```go
func Node() Node
```

- *Type:* github.com/aws/constructs-go/constructs/v10.Node

The tree node.

---

##### `Env`<sup>Required</sup> <a name="Env" id="cdk-constructs.ThronEc2Service.property.env"></a>

```go
func Env() ResourceEnvironment
```

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.ResourceEnvironment

The environment this resource belongs to.

For resources that are created and managed by the CDK
(generally, those created by creating new class instances like Role, Bucket, etc.),
this is always the same as the environment of the stack they belong to;
however, for imported resources
(those obtained from static methods like fromRoleArn, fromBucketName, etc.),
that might be different than the stack they were imported into.

---

##### `Stack`<sup>Required</sup> <a name="Stack" id="cdk-constructs.ThronEc2Service.property.stack"></a>

```go
func Stack() Stack
```

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.Stack

The stack in which this resource is defined.

---

##### `Cluster`<sup>Required</sup> <a name="Cluster" id="cdk-constructs.ThronEc2Service.property.cluster"></a>

```go
func Cluster() ICluster
```

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_ecs.ICluster

The cluster that hosts the service.

---

##### `Connections`<sup>Required</sup> <a name="Connections" id="cdk-constructs.ThronEc2Service.property.connections"></a>

```go
func Connections() Connections
```

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_ec2.Connections

The security groups which manage the allowed network traffic for the service.

---

##### `ServiceArn`<sup>Required</sup> <a name="ServiceArn" id="cdk-constructs.ThronEc2Service.property.serviceArn"></a>

```go
func ServiceArn() *string
```

- *Type:* *string

The Amazon Resource Name (ARN) of the service.

---

##### `ServiceName`<sup>Required</sup> <a name="ServiceName" id="cdk-constructs.ThronEc2Service.property.serviceName"></a>

```go
func ServiceName() *string
```

- *Type:* *string

The name of the service.

---

##### `TaskDefinition`<sup>Required</sup> <a name="TaskDefinition" id="cdk-constructs.ThronEc2Service.property.taskDefinition"></a>

```go
func TaskDefinition() TaskDefinition
```

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_ecs.TaskDefinition

The task definition to use for tasks in the service.

---

##### `CloudMapService`<sup>Optional</sup> <a name="CloudMapService" id="cdk-constructs.ThronEc2Service.property.cloudMapService"></a>

```go
func CloudMapService() IService
```

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_servicediscovery.IService

The CloudMap service created for this service, if any.

---

##### `Ec2TaskDefinition`<sup>Required</sup> <a name="Ec2TaskDefinition" id="cdk-constructs.ThronEc2Service.property.ec2TaskDefinition"></a>

```go
func Ec2TaskDefinition() ThronEc2TaskDefinition
```

- *Type:* <a href="#cdk-constructs.ThronEc2TaskDefinition">ThronEc2TaskDefinition</a>

---

##### `Endpoints`<sup>Optional</sup> <a name="Endpoints" id="cdk-constructs.ThronEc2Service.property.endpoints"></a>

```go
func Endpoints() *map[string]EndpointAlb
```

- *Type:* *map[string]<a href="#cdk-constructs.EndpointAlb">EndpointAlb</a>

---

##### `LegacyEndpoints`<sup>Optional</sup> <a name="LegacyEndpoints" id="cdk-constructs.ThronEc2Service.property.legacyEndpoints"></a>

```go
func LegacyEndpoints() *map[string]EndpointAlb
```

- *Type:* *map[string]<a href="#cdk-constructs.EndpointAlb">EndpointAlb</a>

---

##### `TargetScaling`<sup>Optional</sup> <a name="TargetScaling" id="cdk-constructs.ThronEc2Service.property.targetScaling"></a>

```go
func TargetScaling() ThronTargetScaling
```

- *Type:* <a href="#cdk-constructs.ThronTargetScaling">ThronTargetScaling</a>

---


### ThronEc2TargetScaling <a name="ThronEc2TargetScaling" id="cdk-constructs.ThronEc2TargetScaling"></a>

#### Initializers <a name="Initializers" id="cdk-constructs.ThronEc2TargetScaling.Initializer"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

cdkconstructs.NewThronEc2TargetScaling(scope Construct, id *string, props ThronEc2TargetScalingProps) ThronEc2TargetScaling
```

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.ThronEc2TargetScaling.Initializer.parameter.scope">scope</a></code> | <code>github.com/aws/constructs-go/constructs/v10.Construct</code> | *No description.* |
| <code><a href="#cdk-constructs.ThronEc2TargetScaling.Initializer.parameter.id">id</a></code> | <code>*string</code> | *No description.* |
| <code><a href="#cdk-constructs.ThronEc2TargetScaling.Initializer.parameter.props">props</a></code> | <code><a href="#cdk-constructs.ThronEc2TargetScalingProps">ThronEc2TargetScalingProps</a></code> | *No description.* |

---

##### `scope`<sup>Required</sup> <a name="scope" id="cdk-constructs.ThronEc2TargetScaling.Initializer.parameter.scope"></a>

- *Type:* github.com/aws/constructs-go/constructs/v10.Construct

---

##### `id`<sup>Required</sup> <a name="id" id="cdk-constructs.ThronEc2TargetScaling.Initializer.parameter.id"></a>

- *Type:* *string

---

##### `props`<sup>Required</sup> <a name="props" id="cdk-constructs.ThronEc2TargetScaling.Initializer.parameter.props"></a>

- *Type:* <a href="#cdk-constructs.ThronEc2TargetScalingProps">ThronEc2TargetScalingProps</a>

---

#### Methods <a name="Methods" id="Methods"></a>

| **Name** | **Description** |
| --- | --- |
| <code><a href="#cdk-constructs.ThronEc2TargetScaling.toString">ToString</a></code> | Returns a string representation of this construct. |

---

##### `ToString` <a name="ToString" id="cdk-constructs.ThronEc2TargetScaling.toString"></a>

```go
func ToString() *string
```

Returns a string representation of this construct.

#### Static Functions <a name="Static Functions" id="Static Functions"></a>

| **Name** | **Description** |
| --- | --- |
| <code><a href="#cdk-constructs.ThronEc2TargetScaling.isConstruct">IsConstruct</a></code> | Checks if `x` is a construct. |

---

##### `IsConstruct` <a name="IsConstruct" id="cdk-constructs.ThronEc2TargetScaling.isConstruct"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

cdkconstructs.ThronEc2TargetScaling_IsConstruct(x interface{}) *bool
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

- *Type:* interface{}

Any object.

---

#### Properties <a name="Properties" id="Properties"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.ThronEc2TargetScaling.property.node">Node</a></code> | <code>github.com/aws/constructs-go/constructs/v10.Node</code> | The tree node. |
| <code><a href="#cdk-constructs.ThronEc2TargetScaling.property.maxCapacity">MaxCapacity</a></code> | <code>*f64</code> | The maximum value that Application Auto Scaling can use to scale a target during a scaling activity. |
| <code><a href="#cdk-constructs.ThronEc2TargetScaling.property.minCapacity">MinCapacity</a></code> | <code>*f64</code> | The minimum value that Application Auto Scaling can use to scale a target during a scaling activity. |
| <code><a href="#cdk-constructs.ThronEc2TargetScaling.property.targetValue">TargetValue</a></code> | <code>*f64</code> | The target value for the metric. |
| <code><a href="#cdk-constructs.ThronEc2TargetScaling.property.predefinedMetric">PredefinedMetric</a></code> | <code>github.com/aws/aws-cdk-go/awscdk/v2.aws_applicationautoscaling.PredefinedMetric</code> | A predefined metric for application autoscaling. |
| <code><a href="#cdk-constructs.ThronEc2TargetScaling.property.ec2Service">Ec2Service</a></code> | <code>github.com/aws/aws-cdk-go/awscdk/v2.aws_ecs.Ec2Service</code> | Ec2 Service used as target resource. |
| <code><a href="#cdk-constructs.ThronEc2TargetScaling.property.scalableTarget">ScalableTarget</a></code> | <code>github.com/aws/aws-cdk-go/awscdk/v2.aws_applicationautoscaling.ScalableTarget</code> | *No description.* |
| <code><a href="#cdk-constructs.ThronEc2TargetScaling.property.targetTrackingScalingPolicy">TargetTrackingScalingPolicy</a></code> | <code>github.com/aws/aws-cdk-go/awscdk/v2.aws_applicationautoscaling.TargetTrackingScalingPolicy</code> | *No description.* |

---

##### `Node`<sup>Required</sup> <a name="Node" id="cdk-constructs.ThronEc2TargetScaling.property.node"></a>

```go
func Node() Node
```

- *Type:* github.com/aws/constructs-go/constructs/v10.Node

The tree node.

---

##### `MaxCapacity`<sup>Required</sup> <a name="MaxCapacity" id="cdk-constructs.ThronEc2TargetScaling.property.maxCapacity"></a>

```go
func MaxCapacity() *f64
```

- *Type:* *f64

The maximum value that Application Auto Scaling can use to scale a target during a scaling activity.

---

##### `MinCapacity`<sup>Required</sup> <a name="MinCapacity" id="cdk-constructs.ThronEc2TargetScaling.property.minCapacity"></a>

```go
func MinCapacity() *f64
```

- *Type:* *f64

The minimum value that Application Auto Scaling can use to scale a target during a scaling activity.

---

##### `TargetValue`<sup>Required</sup> <a name="TargetValue" id="cdk-constructs.ThronEc2TargetScaling.property.targetValue"></a>

```go
func TargetValue() *f64
```

- *Type:* *f64

The target value for the metric.

---

##### `PredefinedMetric`<sup>Optional</sup> <a name="PredefinedMetric" id="cdk-constructs.ThronEc2TargetScaling.property.predefinedMetric"></a>

```go
func PredefinedMetric() PredefinedMetric
```

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_applicationautoscaling.PredefinedMetric

A predefined metric for application autoscaling.

The metric must track utilization. Scaling out will happen if the metric is higher than the target value,
scaling in will happen in the metric is lower than the target value.

---

##### `Ec2Service`<sup>Required</sup> <a name="Ec2Service" id="cdk-constructs.ThronEc2TargetScaling.property.ec2Service"></a>

```go
func Ec2Service() Ec2Service
```

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_ecs.Ec2Service

Ec2 Service used as target resource.

---

##### `ScalableTarget`<sup>Required</sup> <a name="ScalableTarget" id="cdk-constructs.ThronEc2TargetScaling.property.scalableTarget"></a>

```go
func ScalableTarget() ScalableTarget
```

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_applicationautoscaling.ScalableTarget

---

##### `TargetTrackingScalingPolicy`<sup>Required</sup> <a name="TargetTrackingScalingPolicy" id="cdk-constructs.ThronEc2TargetScaling.property.targetTrackingScalingPolicy"></a>

```go
func TargetTrackingScalingPolicy() TargetTrackingScalingPolicy
```

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_applicationautoscaling.TargetTrackingScalingPolicy

---


### ThronEc2TaskDefinition <a name="ThronEc2TaskDefinition" id="cdk-constructs.ThronEc2TaskDefinition"></a>

#### Initializers <a name="Initializers" id="cdk-constructs.ThronEc2TaskDefinition.Initializer"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

cdkconstructs.NewThronEc2TaskDefinition(scope Stack, id *string, props ThronEc2TaskDefinitionProps) ThronEc2TaskDefinition
```

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.ThronEc2TaskDefinition.Initializer.parameter.scope">scope</a></code> | <code>github.com/aws/aws-cdk-go/awscdk/v2.Stack</code> | *No description.* |
| <code><a href="#cdk-constructs.ThronEc2TaskDefinition.Initializer.parameter.id">id</a></code> | <code>*string</code> | *No description.* |
| <code><a href="#cdk-constructs.ThronEc2TaskDefinition.Initializer.parameter.props">props</a></code> | <code><a href="#cdk-constructs.ThronEc2TaskDefinitionProps">ThronEc2TaskDefinitionProps</a></code> | *No description.* |

---

##### `scope`<sup>Required</sup> <a name="scope" id="cdk-constructs.ThronEc2TaskDefinition.Initializer.parameter.scope"></a>

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.Stack

---

##### `id`<sup>Required</sup> <a name="id" id="cdk-constructs.ThronEc2TaskDefinition.Initializer.parameter.id"></a>

- *Type:* *string

---

##### `props`<sup>Required</sup> <a name="props" id="cdk-constructs.ThronEc2TaskDefinition.Initializer.parameter.props"></a>

- *Type:* <a href="#cdk-constructs.ThronEc2TaskDefinitionProps">ThronEc2TaskDefinitionProps</a>

---

#### Methods <a name="Methods" id="Methods"></a>

| **Name** | **Description** |
| --- | --- |
| <code><a href="#cdk-constructs.ThronEc2TaskDefinition.toString">ToString</a></code> | Returns a string representation of this construct. |
| <code><a href="#cdk-constructs.ThronEc2TaskDefinition.applyRemovalPolicy">ApplyRemovalPolicy</a></code> | Apply the given removal policy to this resource. |
| <code><a href="#cdk-constructs.ThronEc2TaskDefinition.addContainer">AddContainer</a></code> | Tasks running in AWSVPC networking mode requires an additional environment variable for the region to be sourced. |
| <code><a href="#cdk-constructs.ThronEc2TaskDefinition.addExtension">AddExtension</a></code> | Adds the specified extension to the task definition. |
| <code><a href="#cdk-constructs.ThronEc2TaskDefinition.addFirelensLogRouter">AddFirelensLogRouter</a></code> | Adds a firelens log router to the task definition. |
| <code><a href="#cdk-constructs.ThronEc2TaskDefinition.addInferenceAccelerator">AddInferenceAccelerator</a></code> | Adds an inference accelerator to the task definition. |
| <code><a href="#cdk-constructs.ThronEc2TaskDefinition.addPlacementConstraint">AddPlacementConstraint</a></code> | Adds the specified placement constraint to the task definition. |
| <code><a href="#cdk-constructs.ThronEc2TaskDefinition.addToExecutionRolePolicy">AddToExecutionRolePolicy</a></code> | Adds a policy statement to the task execution IAM role. |
| <code><a href="#cdk-constructs.ThronEc2TaskDefinition.addToTaskRolePolicy">AddToTaskRolePolicy</a></code> | Adds a policy statement to the task IAM role. |
| <code><a href="#cdk-constructs.ThronEc2TaskDefinition.addVolume">AddVolume</a></code> | Adds a volume to the task definition. |
| <code><a href="#cdk-constructs.ThronEc2TaskDefinition.findContainer">FindContainer</a></code> | Returns the container that match the provided containerName. |
| <code><a href="#cdk-constructs.ThronEc2TaskDefinition.findPortMappingByName">FindPortMappingByName</a></code> | Determine the existing port mapping for the provided name. |
| <code><a href="#cdk-constructs.ThronEc2TaskDefinition.grantRun">GrantRun</a></code> | Grants permissions to run this task definition. |
| <code><a href="#cdk-constructs.ThronEc2TaskDefinition.obtainExecutionRole">ObtainExecutionRole</a></code> | Creates the task execution IAM role if it doesn't already exist. |

---

##### `ToString` <a name="ToString" id="cdk-constructs.ThronEc2TaskDefinition.toString"></a>

```go
func ToString() *string
```

Returns a string representation of this construct.

##### `ApplyRemovalPolicy` <a name="ApplyRemovalPolicy" id="cdk-constructs.ThronEc2TaskDefinition.applyRemovalPolicy"></a>

```go
func ApplyRemovalPolicy(policy RemovalPolicy)
```

Apply the given removal policy to this resource.

The Removal Policy controls what happens to this resource when it stops
being managed by CloudFormation, either because you've removed it from the
CDK application or because you've made a change that requires the resource
to be replaced.

The resource can be deleted (`RemovalPolicy.DESTROY`), or left in your AWS
account for data recovery and cleanup later (`RemovalPolicy.RETAIN`).

###### `policy`<sup>Required</sup> <a name="policy" id="cdk-constructs.ThronEc2TaskDefinition.applyRemovalPolicy.parameter.policy"></a>

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.RemovalPolicy

---

##### `AddContainer` <a name="AddContainer" id="cdk-constructs.ThronEc2TaskDefinition.addContainer"></a>

```go
func AddContainer(id *string, props ContainerDefinitionOptions) ContainerDefinition
```

Tasks running in AWSVPC networking mode requires an additional environment variable for the region to be sourced.

This override adds in the additional environment variable as required

###### `id`<sup>Required</sup> <a name="id" id="cdk-constructs.ThronEc2TaskDefinition.addContainer.parameter.id"></a>

- *Type:* *string

---

###### `props`<sup>Required</sup> <a name="props" id="cdk-constructs.ThronEc2TaskDefinition.addContainer.parameter.props"></a>

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_ecs.ContainerDefinitionOptions

---

##### `AddExtension` <a name="AddExtension" id="cdk-constructs.ThronEc2TaskDefinition.addExtension"></a>

```go
func AddExtension(extension ITaskDefinitionExtension)
```

Adds the specified extension to the task definition.

Extension can be used to apply a packaged modification to
a task definition.

###### `extension`<sup>Required</sup> <a name="extension" id="cdk-constructs.ThronEc2TaskDefinition.addExtension.parameter.extension"></a>

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_ecs.ITaskDefinitionExtension

---

##### `AddFirelensLogRouter` <a name="AddFirelensLogRouter" id="cdk-constructs.ThronEc2TaskDefinition.addFirelensLogRouter"></a>

```go
func AddFirelensLogRouter(id *string, props FirelensLogRouterDefinitionOptions) FirelensLogRouter
```

Adds a firelens log router to the task definition.

###### `id`<sup>Required</sup> <a name="id" id="cdk-constructs.ThronEc2TaskDefinition.addFirelensLogRouter.parameter.id"></a>

- *Type:* *string

---

###### `props`<sup>Required</sup> <a name="props" id="cdk-constructs.ThronEc2TaskDefinition.addFirelensLogRouter.parameter.props"></a>

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_ecs.FirelensLogRouterDefinitionOptions

---

##### ~~`AddInferenceAccelerator`~~ <a name="AddInferenceAccelerator" id="cdk-constructs.ThronEc2TaskDefinition.addInferenceAccelerator"></a>

```go
func AddInferenceAccelerator(inferenceAccelerator InferenceAccelerator)
```

Adds an inference accelerator to the task definition.

###### `inferenceAccelerator`<sup>Required</sup> <a name="inferenceAccelerator" id="cdk-constructs.ThronEc2TaskDefinition.addInferenceAccelerator.parameter.inferenceAccelerator"></a>

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_ecs.InferenceAccelerator

---

##### `AddPlacementConstraint` <a name="AddPlacementConstraint" id="cdk-constructs.ThronEc2TaskDefinition.addPlacementConstraint"></a>

```go
func AddPlacementConstraint(constraint PlacementConstraint)
```

Adds the specified placement constraint to the task definition.

###### `constraint`<sup>Required</sup> <a name="constraint" id="cdk-constructs.ThronEc2TaskDefinition.addPlacementConstraint.parameter.constraint"></a>

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_ecs.PlacementConstraint

---

##### `AddToExecutionRolePolicy` <a name="AddToExecutionRolePolicy" id="cdk-constructs.ThronEc2TaskDefinition.addToExecutionRolePolicy"></a>

```go
func AddToExecutionRolePolicy(statement PolicyStatement)
```

Adds a policy statement to the task execution IAM role.

###### `statement`<sup>Required</sup> <a name="statement" id="cdk-constructs.ThronEc2TaskDefinition.addToExecutionRolePolicy.parameter.statement"></a>

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_iam.PolicyStatement

---

##### `AddToTaskRolePolicy` <a name="AddToTaskRolePolicy" id="cdk-constructs.ThronEc2TaskDefinition.addToTaskRolePolicy"></a>

```go
func AddToTaskRolePolicy(statement PolicyStatement)
```

Adds a policy statement to the task IAM role.

###### `statement`<sup>Required</sup> <a name="statement" id="cdk-constructs.ThronEc2TaskDefinition.addToTaskRolePolicy.parameter.statement"></a>

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_iam.PolicyStatement

---

##### `AddVolume` <a name="AddVolume" id="cdk-constructs.ThronEc2TaskDefinition.addVolume"></a>

```go
func AddVolume(volume Volume)
```

Adds a volume to the task definition.

###### `volume`<sup>Required</sup> <a name="volume" id="cdk-constructs.ThronEc2TaskDefinition.addVolume.parameter.volume"></a>

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_ecs.Volume

---

##### `FindContainer` <a name="FindContainer" id="cdk-constructs.ThronEc2TaskDefinition.findContainer"></a>

```go
func FindContainer(containerName *string) ContainerDefinition
```

Returns the container that match the provided containerName.

###### `containerName`<sup>Required</sup> <a name="containerName" id="cdk-constructs.ThronEc2TaskDefinition.findContainer.parameter.containerName"></a>

- *Type:* *string

---

##### `FindPortMappingByName` <a name="FindPortMappingByName" id="cdk-constructs.ThronEc2TaskDefinition.findPortMappingByName"></a>

```go
func FindPortMappingByName(name *string) PortMapping
```

Determine the existing port mapping for the provided name.

###### `name`<sup>Required</sup> <a name="name" id="cdk-constructs.ThronEc2TaskDefinition.findPortMappingByName.parameter.name"></a>

- *Type:* *string

: port mapping name.

---

##### `GrantRun` <a name="GrantRun" id="cdk-constructs.ThronEc2TaskDefinition.grantRun"></a>

```go
func GrantRun(grantee IGrantable) Grant
```

Grants permissions to run this task definition.

This will grant the following permissions:

  - ecs:RunTask
  - iam:PassRole

###### `grantee`<sup>Required</sup> <a name="grantee" id="cdk-constructs.ThronEc2TaskDefinition.grantRun.parameter.grantee"></a>

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_iam.IGrantable

Principal to grant consume rights to.

---

##### `ObtainExecutionRole` <a name="ObtainExecutionRole" id="cdk-constructs.ThronEc2TaskDefinition.obtainExecutionRole"></a>

```go
func ObtainExecutionRole() IRole
```

Creates the task execution IAM role if it doesn't already exist.

#### Static Functions <a name="Static Functions" id="Static Functions"></a>

| **Name** | **Description** |
| --- | --- |
| <code><a href="#cdk-constructs.ThronEc2TaskDefinition.isConstruct">IsConstruct</a></code> | Checks if `x` is a construct. |
| <code><a href="#cdk-constructs.ThronEc2TaskDefinition.isOwnedResource">IsOwnedResource</a></code> | Returns true if the construct was created by CDK, and false otherwise. |
| <code><a href="#cdk-constructs.ThronEc2TaskDefinition.isResource">IsResource</a></code> | Check whether the given construct is a Resource. |
| <code><a href="#cdk-constructs.ThronEc2TaskDefinition.fromTaskDefinitionArn">FromTaskDefinitionArn</a></code> | Imports a task definition from the specified task definition ARN. |
| <code><a href="#cdk-constructs.ThronEc2TaskDefinition.fromTaskDefinitionAttributes">FromTaskDefinitionAttributes</a></code> | Create a task definition from a task definition reference. |
| <code><a href="#cdk-constructs.ThronEc2TaskDefinition.fromEc2TaskDefinitionArn">FromEc2TaskDefinitionArn</a></code> | Imports a task definition from the specified task definition ARN. |
| <code><a href="#cdk-constructs.ThronEc2TaskDefinition.fromEc2TaskDefinitionAttributes">FromEc2TaskDefinitionAttributes</a></code> | Imports an existing Ec2 task definition from its attributes. |

---

##### `IsConstruct` <a name="IsConstruct" id="cdk-constructs.ThronEc2TaskDefinition.isConstruct"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

cdkconstructs.ThronEc2TaskDefinition_IsConstruct(x interface{}) *bool
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

- *Type:* interface{}

Any object.

---

##### `IsOwnedResource` <a name="IsOwnedResource" id="cdk-constructs.ThronEc2TaskDefinition.isOwnedResource"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

cdkconstructs.ThronEc2TaskDefinition_IsOwnedResource(construct IConstruct) *bool
```

Returns true if the construct was created by CDK, and false otherwise.

###### `construct`<sup>Required</sup> <a name="construct" id="cdk-constructs.ThronEc2TaskDefinition.isOwnedResource.parameter.construct"></a>

- *Type:* github.com/aws/constructs-go/constructs/v10.IConstruct

---

##### `IsResource` <a name="IsResource" id="cdk-constructs.ThronEc2TaskDefinition.isResource"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

cdkconstructs.ThronEc2TaskDefinition_IsResource(construct IConstruct) *bool
```

Check whether the given construct is a Resource.

###### `construct`<sup>Required</sup> <a name="construct" id="cdk-constructs.ThronEc2TaskDefinition.isResource.parameter.construct"></a>

- *Type:* github.com/aws/constructs-go/constructs/v10.IConstruct

---

##### `FromTaskDefinitionArn` <a name="FromTaskDefinitionArn" id="cdk-constructs.ThronEc2TaskDefinition.fromTaskDefinitionArn"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

cdkconstructs.ThronEc2TaskDefinition_FromTaskDefinitionArn(scope Construct, id *string, taskDefinitionArn *string) ITaskDefinition
```

Imports a task definition from the specified task definition ARN.

The task will have a compatibility of EC2+Fargate.

###### `scope`<sup>Required</sup> <a name="scope" id="cdk-constructs.ThronEc2TaskDefinition.fromTaskDefinitionArn.parameter.scope"></a>

- *Type:* github.com/aws/constructs-go/constructs/v10.Construct

---

###### `id`<sup>Required</sup> <a name="id" id="cdk-constructs.ThronEc2TaskDefinition.fromTaskDefinitionArn.parameter.id"></a>

- *Type:* *string

---

###### `taskDefinitionArn`<sup>Required</sup> <a name="taskDefinitionArn" id="cdk-constructs.ThronEc2TaskDefinition.fromTaskDefinitionArn.parameter.taskDefinitionArn"></a>

- *Type:* *string

---

##### `FromTaskDefinitionAttributes` <a name="FromTaskDefinitionAttributes" id="cdk-constructs.ThronEc2TaskDefinition.fromTaskDefinitionAttributes"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

cdkconstructs.ThronEc2TaskDefinition_FromTaskDefinitionAttributes(scope Construct, id *string, attrs TaskDefinitionAttributes) ITaskDefinition
```

Create a task definition from a task definition reference.

###### `scope`<sup>Required</sup> <a name="scope" id="cdk-constructs.ThronEc2TaskDefinition.fromTaskDefinitionAttributes.parameter.scope"></a>

- *Type:* github.com/aws/constructs-go/constructs/v10.Construct

---

###### `id`<sup>Required</sup> <a name="id" id="cdk-constructs.ThronEc2TaskDefinition.fromTaskDefinitionAttributes.parameter.id"></a>

- *Type:* *string

---

###### `attrs`<sup>Required</sup> <a name="attrs" id="cdk-constructs.ThronEc2TaskDefinition.fromTaskDefinitionAttributes.parameter.attrs"></a>

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_ecs.TaskDefinitionAttributes

---

##### `FromEc2TaskDefinitionArn` <a name="FromEc2TaskDefinitionArn" id="cdk-constructs.ThronEc2TaskDefinition.fromEc2TaskDefinitionArn"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

cdkconstructs.ThronEc2TaskDefinition_FromEc2TaskDefinitionArn(scope Construct, id *string, ec2TaskDefinitionArn *string) IEc2TaskDefinition
```

Imports a task definition from the specified task definition ARN.

###### `scope`<sup>Required</sup> <a name="scope" id="cdk-constructs.ThronEc2TaskDefinition.fromEc2TaskDefinitionArn.parameter.scope"></a>

- *Type:* github.com/aws/constructs-go/constructs/v10.Construct

---

###### `id`<sup>Required</sup> <a name="id" id="cdk-constructs.ThronEc2TaskDefinition.fromEc2TaskDefinitionArn.parameter.id"></a>

- *Type:* *string

---

###### `ec2TaskDefinitionArn`<sup>Required</sup> <a name="ec2TaskDefinitionArn" id="cdk-constructs.ThronEc2TaskDefinition.fromEc2TaskDefinitionArn.parameter.ec2TaskDefinitionArn"></a>

- *Type:* *string

---

##### `FromEc2TaskDefinitionAttributes` <a name="FromEc2TaskDefinitionAttributes" id="cdk-constructs.ThronEc2TaskDefinition.fromEc2TaskDefinitionAttributes"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

cdkconstructs.ThronEc2TaskDefinition_FromEc2TaskDefinitionAttributes(scope Construct, id *string, attrs Ec2TaskDefinitionAttributes) IEc2TaskDefinition
```

Imports an existing Ec2 task definition from its attributes.

###### `scope`<sup>Required</sup> <a name="scope" id="cdk-constructs.ThronEc2TaskDefinition.fromEc2TaskDefinitionAttributes.parameter.scope"></a>

- *Type:* github.com/aws/constructs-go/constructs/v10.Construct

---

###### `id`<sup>Required</sup> <a name="id" id="cdk-constructs.ThronEc2TaskDefinition.fromEc2TaskDefinitionAttributes.parameter.id"></a>

- *Type:* *string

---

###### `attrs`<sup>Required</sup> <a name="attrs" id="cdk-constructs.ThronEc2TaskDefinition.fromEc2TaskDefinitionAttributes.parameter.attrs"></a>

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_ecs.Ec2TaskDefinitionAttributes

---

#### Properties <a name="Properties" id="Properties"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.ThronEc2TaskDefinition.property.node">Node</a></code> | <code>github.com/aws/constructs-go/constructs/v10.Node</code> | The tree node. |
| <code><a href="#cdk-constructs.ThronEc2TaskDefinition.property.env">Env</a></code> | <code>github.com/aws/aws-cdk-go/awscdk/v2.ResourceEnvironment</code> | The environment this resource belongs to. |
| <code><a href="#cdk-constructs.ThronEc2TaskDefinition.property.stack">Stack</a></code> | <code>github.com/aws/aws-cdk-go/awscdk/v2.Stack</code> | The stack in which this resource is defined. |
| <code><a href="#cdk-constructs.ThronEc2TaskDefinition.property.compatibility">Compatibility</a></code> | <code>github.com/aws/aws-cdk-go/awscdk/v2.aws_ecs.Compatibility</code> | The task launch type compatibility requirement. |
| <code><a href="#cdk-constructs.ThronEc2TaskDefinition.property.family">Family</a></code> | <code>*string</code> | The name of a family that this task definition is registered to. |
| <code><a href="#cdk-constructs.ThronEc2TaskDefinition.property.inferenceAccelerators">InferenceAccelerators</a></code> | <code>*[]github.com/aws/aws-cdk-go/awscdk/v2.aws_ecs.InferenceAccelerator</code> | Public getter method to access list of inference accelerators attached to the instance. |
| <code><a href="#cdk-constructs.ThronEc2TaskDefinition.property.isEc2Compatible">IsEc2Compatible</a></code> | <code>*bool</code> | Return true if the task definition can be run on an EC2 cluster. |
| <code><a href="#cdk-constructs.ThronEc2TaskDefinition.property.isExternalCompatible">IsExternalCompatible</a></code> | <code>*bool</code> | Return true if the task definition can be run on a ECS anywhere cluster. |
| <code><a href="#cdk-constructs.ThronEc2TaskDefinition.property.isFargateCompatible">IsFargateCompatible</a></code> | <code>*bool</code> | Return true if the task definition can be run on a Fargate cluster. |
| <code><a href="#cdk-constructs.ThronEc2TaskDefinition.property.networkMode">NetworkMode</a></code> | <code>github.com/aws/aws-cdk-go/awscdk/v2.aws_ecs.NetworkMode</code> | The networking mode to use for the containers in the task. |
| <code><a href="#cdk-constructs.ThronEc2TaskDefinition.property.taskDefinitionArn">TaskDefinitionArn</a></code> | <code>*string</code> | The full Amazon Resource Name (ARN) of the task definition. |
| <code><a href="#cdk-constructs.ThronEc2TaskDefinition.property.taskRole">TaskRole</a></code> | <code>github.com/aws/aws-cdk-go/awscdk/v2.aws_iam.IRole</code> | The name of the IAM role that grants containers in the task permission to call AWS APIs on your behalf. |
| <code><a href="#cdk-constructs.ThronEc2TaskDefinition.property.ephemeralStorageGiB">EphemeralStorageGiB</a></code> | <code>*f64</code> | The amount (in GiB) of ephemeral storage to be allocated to the task. |
| <code><a href="#cdk-constructs.ThronEc2TaskDefinition.property.executionRole">ExecutionRole</a></code> | <code>github.com/aws/aws-cdk-go/awscdk/v2.aws_iam.IRole</code> | Execution role for this task definition. |
| <code><a href="#cdk-constructs.ThronEc2TaskDefinition.property.pidMode">PidMode</a></code> | <code>github.com/aws/aws-cdk-go/awscdk/v2.aws_ecs.PidMode</code> | The process namespace to use for the containers in the task. |
| <code><a href="#cdk-constructs.ThronEc2TaskDefinition.property.referencesSecretJsonField">ReferencesSecretJsonField</a></code> | <code>*bool</code> | Whether this task definition has at least a container that references a specific JSON field of a secret stored in Secrets Manager. |
| <code><a href="#cdk-constructs.ThronEc2TaskDefinition.property.defaultContainer">DefaultContainer</a></code> | <code>github.com/aws/aws-cdk-go/awscdk/v2.aws_ecs.ContainerDefinition</code> | Default container for this task. |
| <code><a href="#cdk-constructs.ThronEc2TaskDefinition.property.container">Container</a></code> | <code>github.com/aws/aws-cdk-go/awscdk/v2.aws_ecs.ContainerDefinition</code> | *No description.* |
| <code><a href="#cdk-constructs.ThronEc2TaskDefinition.property.logs">Logs</a></code> | <code>github.com/aws/aws-cdk-go/awscdk/v2.aws_logs.LogGroup</code> | *No description.* |
| <code><a href="#cdk-constructs.ThronEc2TaskDefinition.property.port">Port</a></code> | <code>*f64</code> | The port exposed for connection. |
| <code><a href="#cdk-constructs.ThronEc2TaskDefinition.property.prometheusMetricsPath">PrometheusMetricsPath</a></code> | <code>*string</code> | *No description.* |

---

##### `Node`<sup>Required</sup> <a name="Node" id="cdk-constructs.ThronEc2TaskDefinition.property.node"></a>

```go
func Node() Node
```

- *Type:* github.com/aws/constructs-go/constructs/v10.Node

The tree node.

---

##### `Env`<sup>Required</sup> <a name="Env" id="cdk-constructs.ThronEc2TaskDefinition.property.env"></a>

```go
func Env() ResourceEnvironment
```

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.ResourceEnvironment

The environment this resource belongs to.

For resources that are created and managed by the CDK
(generally, those created by creating new class instances like Role, Bucket, etc.),
this is always the same as the environment of the stack they belong to;
however, for imported resources
(those obtained from static methods like fromRoleArn, fromBucketName, etc.),
that might be different than the stack they were imported into.

---

##### `Stack`<sup>Required</sup> <a name="Stack" id="cdk-constructs.ThronEc2TaskDefinition.property.stack"></a>

```go
func Stack() Stack
```

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.Stack

The stack in which this resource is defined.

---

##### `Compatibility`<sup>Required</sup> <a name="Compatibility" id="cdk-constructs.ThronEc2TaskDefinition.property.compatibility"></a>

```go
func Compatibility() Compatibility
```

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_ecs.Compatibility

The task launch type compatibility requirement.

---

##### `Family`<sup>Required</sup> <a name="Family" id="cdk-constructs.ThronEc2TaskDefinition.property.family"></a>

```go
func Family() *string
```

- *Type:* *string

The name of a family that this task definition is registered to.

A family groups multiple versions of a task definition.

---

##### `InferenceAccelerators`<sup>Required</sup> <a name="InferenceAccelerators" id="cdk-constructs.ThronEc2TaskDefinition.property.inferenceAccelerators"></a>

```go
func InferenceAccelerators() *[]InferenceAccelerator
```

- *Type:* *[]github.com/aws/aws-cdk-go/awscdk/v2.aws_ecs.InferenceAccelerator

Public getter method to access list of inference accelerators attached to the instance.

---

##### `IsEc2Compatible`<sup>Required</sup> <a name="IsEc2Compatible" id="cdk-constructs.ThronEc2TaskDefinition.property.isEc2Compatible"></a>

```go
func IsEc2Compatible() *bool
```

- *Type:* *bool

Return true if the task definition can be run on an EC2 cluster.

---

##### `IsExternalCompatible`<sup>Required</sup> <a name="IsExternalCompatible" id="cdk-constructs.ThronEc2TaskDefinition.property.isExternalCompatible"></a>

```go
func IsExternalCompatible() *bool
```

- *Type:* *bool

Return true if the task definition can be run on a ECS anywhere cluster.

---

##### `IsFargateCompatible`<sup>Required</sup> <a name="IsFargateCompatible" id="cdk-constructs.ThronEc2TaskDefinition.property.isFargateCompatible"></a>

```go
func IsFargateCompatible() *bool
```

- *Type:* *bool

Return true if the task definition can be run on a Fargate cluster.

---

##### `NetworkMode`<sup>Required</sup> <a name="NetworkMode" id="cdk-constructs.ThronEc2TaskDefinition.property.networkMode"></a>

```go
func NetworkMode() NetworkMode
```

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_ecs.NetworkMode

The networking mode to use for the containers in the task.

---

##### `TaskDefinitionArn`<sup>Required</sup> <a name="TaskDefinitionArn" id="cdk-constructs.ThronEc2TaskDefinition.property.taskDefinitionArn"></a>

```go
func TaskDefinitionArn() *string
```

- *Type:* *string

The full Amazon Resource Name (ARN) of the task definition.

---

##### `TaskRole`<sup>Required</sup> <a name="TaskRole" id="cdk-constructs.ThronEc2TaskDefinition.property.taskRole"></a>

```go
func TaskRole() IRole
```

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_iam.IRole

The name of the IAM role that grants containers in the task permission to call AWS APIs on your behalf.

---

##### `EphemeralStorageGiB`<sup>Optional</sup> <a name="EphemeralStorageGiB" id="cdk-constructs.ThronEc2TaskDefinition.property.ephemeralStorageGiB"></a>

```go
func EphemeralStorageGiB() *f64
```

- *Type:* *f64

The amount (in GiB) of ephemeral storage to be allocated to the task.

Only supported in Fargate platform version 1.4.0 or later.

---

##### `ExecutionRole`<sup>Optional</sup> <a name="ExecutionRole" id="cdk-constructs.ThronEc2TaskDefinition.property.executionRole"></a>

```go
func ExecutionRole() IRole
```

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_iam.IRole

Execution role for this task definition.

---

##### `PidMode`<sup>Optional</sup> <a name="PidMode" id="cdk-constructs.ThronEc2TaskDefinition.property.pidMode"></a>

```go
func PidMode() PidMode
```

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_ecs.PidMode

The process namespace to use for the containers in the task.

Only supported for tasks that are hosted on AWS Fargate if the tasks
are using platform version 1.4.0 or later (Linux). Not supported in
Windows containers. If pidMode is specified for a Fargate task,
then runtimePlatform.operatingSystemFamily must also be specified.  For more
information, see [Task Definition Parameters](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/task_definition_parameters.html#task_definition_pidmode).

---

##### `ReferencesSecretJsonField`<sup>Optional</sup> <a name="ReferencesSecretJsonField" id="cdk-constructs.ThronEc2TaskDefinition.property.referencesSecretJsonField"></a>

```go
func ReferencesSecretJsonField() *bool
```

- *Type:* *bool

Whether this task definition has at least a container that references a specific JSON field of a secret stored in Secrets Manager.

---

##### `DefaultContainer`<sup>Optional</sup> <a name="DefaultContainer" id="cdk-constructs.ThronEc2TaskDefinition.property.defaultContainer"></a>

```go
func DefaultContainer() ContainerDefinition
```

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_ecs.ContainerDefinition

Default container for this task.

Load balancers will send traffic to this container. The first
essential container that is added to this task will become the default
container.

---

##### `Container`<sup>Required</sup> <a name="Container" id="cdk-constructs.ThronEc2TaskDefinition.property.container"></a>

```go
func Container() ContainerDefinition
```

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_ecs.ContainerDefinition

---

##### `Logs`<sup>Required</sup> <a name="Logs" id="cdk-constructs.ThronEc2TaskDefinition.property.logs"></a>

```go
func Logs() LogGroup
```

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_logs.LogGroup

---

##### `Port`<sup>Optional</sup> <a name="Port" id="cdk-constructs.ThronEc2TaskDefinition.property.port"></a>

```go
func Port() *f64
```

- *Type:* *f64

The port exposed for connection.

---

##### `PrometheusMetricsPath`<sup>Optional</sup> <a name="PrometheusMetricsPath" id="cdk-constructs.ThronEc2TaskDefinition.property.prometheusMetricsPath"></a>

```go
func PrometheusMetricsPath() *string
```

- *Type:* *string

---


### ThronEndpointApiGateway <a name="ThronEndpointApiGateway" id="cdk-constructs.ThronEndpointApiGateway"></a>

This constructs creates an API Gateway Endpoint for a Lambda Function.

It takes care
of creating also its domain following THRON's convention.

#### Initializers <a name="Initializers" id="cdk-constructs.ThronEndpointApiGateway.Initializer"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

cdkconstructs.NewThronEndpointApiGateway(scope Construct, id *string, props ThronEndpointApiGatewayProps) ThronEndpointApiGateway
```

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.ThronEndpointApiGateway.Initializer.parameter.scope">scope</a></code> | <code>github.com/aws/constructs-go/constructs/v10.Construct</code> | *No description.* |
| <code><a href="#cdk-constructs.ThronEndpointApiGateway.Initializer.parameter.id">id</a></code> | <code>*string</code> | *No description.* |
| <code><a href="#cdk-constructs.ThronEndpointApiGateway.Initializer.parameter.props">props</a></code> | <code><a href="#cdk-constructs.ThronEndpointApiGatewayProps">ThronEndpointApiGatewayProps</a></code> | *No description.* |

---

##### `scope`<sup>Required</sup> <a name="scope" id="cdk-constructs.ThronEndpointApiGateway.Initializer.parameter.scope"></a>

- *Type:* github.com/aws/constructs-go/constructs/v10.Construct

---

##### `id`<sup>Required</sup> <a name="id" id="cdk-constructs.ThronEndpointApiGateway.Initializer.parameter.id"></a>

- *Type:* *string

---

##### `props`<sup>Required</sup> <a name="props" id="cdk-constructs.ThronEndpointApiGateway.Initializer.parameter.props"></a>

- *Type:* <a href="#cdk-constructs.ThronEndpointApiGatewayProps">ThronEndpointApiGatewayProps</a>

---

#### Methods <a name="Methods" id="Methods"></a>

| **Name** | **Description** |
| --- | --- |
| <code><a href="#cdk-constructs.ThronEndpointApiGateway.toString">ToString</a></code> | Returns a string representation of this construct. |

---

##### `ToString` <a name="ToString" id="cdk-constructs.ThronEndpointApiGateway.toString"></a>

```go
func ToString() *string
```

Returns a string representation of this construct.

#### Static Functions <a name="Static Functions" id="Static Functions"></a>

| **Name** | **Description** |
| --- | --- |
| <code><a href="#cdk-constructs.ThronEndpointApiGateway.isConstruct">IsConstruct</a></code> | Checks if `x` is a construct. |

---

##### `IsConstruct` <a name="IsConstruct" id="cdk-constructs.ThronEndpointApiGateway.isConstruct"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

cdkconstructs.ThronEndpointApiGateway_IsConstruct(x interface{}) *bool
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

- *Type:* interface{}

Any object.

---

#### Properties <a name="Properties" id="Properties"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.ThronEndpointApiGateway.property.node">Node</a></code> | <code>github.com/aws/constructs-go/constructs/v10.Node</code> | The tree node. |

---

##### `Node`<sup>Required</sup> <a name="Node" id="cdk-constructs.ThronEndpointApiGateway.property.node"></a>

```go
func Node() Node
```

- *Type:* github.com/aws/constructs-go/constructs/v10.Node

The tree node.

---


### ThronLambdaMicroservicePipeline <a name="ThronLambdaMicroservicePipeline" id="cdk-constructs.ThronLambdaMicroservicePipeline"></a>

Construct creating a multi environment pipeline.

*Example*

```go
// Example automatically generated from non-compiling source. May contain errors.
projectId := "productsynctest"
prefix := projectId

// Construct a custom image to be used for the build
defaultBuildImage := thronLambdaMicroservicePipeline_BuildImageFromDockerfile(this,
fmt.Sprintf("%v-cicd-build-docker", prefix), path.join(__dirname, jsii.String("../Docker/build-image")))

// Import an image from another repo
superSpecialImage := thronLambdaMicroservicePipeline_BuildImageFromRepository(this, jsii.String("super-special-repo"), jsii.String("v1.2.1"))

// Pipeline Instantiation
testConstruct := NewThronLambdaMicroservicePipeline(this, fmt.Sprintf("%v-cicd-pipeline-project", prefix), map[string]interface{}{
	"projectId": jsii.String(projectId),
	"customBuildImage": defaultBuildImage,
	"preExistingArtifactBucket": jsii.String("very-special-bucket"),
	"lambdas": map[string]map[string]interface{}{
		"eventemitter": map[string]interface{}{
		},
		"http": map[string]interface{}{
		},
		"importprocessing": map[string]interface{}{
		},
		// Step with additional env variables
		"importvalidation": map[string]map[string]map[string]*string{
			"environmentalVariables": map[string]map[string]*string{
				"specialVar": map[string]*string{
					"value": jsii.String("YEAH"),
				},
			},
		},
		"export": map[string]interface{}{
		},
	},
	"tests": map[string]map[string]interface{}{
		// Step with custom build image
		"Docs": map[string]interface{}{
			"customBuildImage": superSpecialImage,
		},
		"Lint": map[string]interface{}{
		},
		// Step with more powerful build container
		"Vuln": map[string]interface{}{
			"computeType": ComputeType_MEDIUM,
		},
		"TestUnit": map[string]interface{}{
		},
		"TestIntegration": map[string]interface{}{
		},
	},
	"cicdConfig": map[string]map[string]interface{}{
		"development": map[string]interface{}{
			"capabilities": []interface{}{
				PipelineCapability_BUILD,
				PipelineCapability_TEST,
				PipelineCapability_NOTIFY_ON_START,
				PipelineCapability_NOTIFY_ON_FAIL,
				PipelineCapability_NOTIFY_ON_SUCCESS,
			},
			"webhookUrl": jsii.String("https://example.com"),
		},
		"quality": map[string][]interface{}{
			"capabilities": []interface{}{
				PipelineCapability_BUILD,
				PipelineCapability_NOTIFY_ON_SUCCESS,
			},
		},
	},
})
```


#### Initializers <a name="Initializers" id="cdk-constructs.ThronLambdaMicroservicePipeline.Initializer"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

cdkconstructs.NewThronLambdaMicroservicePipeline(scope Construct, id *string, props ThronLambdaMicroservicePipelineProps) ThronLambdaMicroservicePipeline
```

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.ThronLambdaMicroservicePipeline.Initializer.parameter.scope">scope</a></code> | <code>github.com/aws/constructs-go/constructs/v10.Construct</code> | *No description.* |
| <code><a href="#cdk-constructs.ThronLambdaMicroservicePipeline.Initializer.parameter.id">id</a></code> | <code>*string</code> | *No description.* |
| <code><a href="#cdk-constructs.ThronLambdaMicroservicePipeline.Initializer.parameter.props">props</a></code> | <code><a href="#cdk-constructs.ThronLambdaMicroservicePipelineProps">ThronLambdaMicroservicePipelineProps</a></code> | *No description.* |

---

##### `scope`<sup>Required</sup> <a name="scope" id="cdk-constructs.ThronLambdaMicroservicePipeline.Initializer.parameter.scope"></a>

- *Type:* github.com/aws/constructs-go/constructs/v10.Construct

---

##### `id`<sup>Required</sup> <a name="id" id="cdk-constructs.ThronLambdaMicroservicePipeline.Initializer.parameter.id"></a>

- *Type:* *string

---

##### `props`<sup>Required</sup> <a name="props" id="cdk-constructs.ThronLambdaMicroservicePipeline.Initializer.parameter.props"></a>

- *Type:* <a href="#cdk-constructs.ThronLambdaMicroservicePipelineProps">ThronLambdaMicroservicePipelineProps</a>

---

#### Methods <a name="Methods" id="Methods"></a>

| **Name** | **Description** |
| --- | --- |
| <code><a href="#cdk-constructs.ThronLambdaMicroservicePipeline.toString">ToString</a></code> | Returns a string representation of this construct. |

---

##### `ToString` <a name="ToString" id="cdk-constructs.ThronLambdaMicroservicePipeline.toString"></a>

```go
func ToString() *string
```

Returns a string representation of this construct.

#### Static Functions <a name="Static Functions" id="Static Functions"></a>

| **Name** | **Description** |
| --- | --- |
| <code><a href="#cdk-constructs.ThronLambdaMicroservicePipeline.isConstruct">IsConstruct</a></code> | Checks if `x` is a construct. |
| <code><a href="#cdk-constructs.ThronLambdaMicroservicePipeline.buildImageFromDockerfile">BuildImageFromDockerfile</a></code> | *No description.* |
| <code><a href="#cdk-constructs.ThronLambdaMicroservicePipeline.buildImageFromRepository">BuildImageFromRepository</a></code> | Constructs a Build Image to be used in the pipeline steps. |

---

##### `IsConstruct` <a name="IsConstruct" id="cdk-constructs.ThronLambdaMicroservicePipeline.isConstruct"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

cdkconstructs.ThronLambdaMicroservicePipeline_IsConstruct(x interface{}) *bool
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

- *Type:* interface{}

Any object.

---

##### `BuildImageFromDockerfile` <a name="BuildImageFromDockerfile" id="cdk-constructs.ThronLambdaMicroservicePipeline.buildImageFromDockerfile"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

cdkconstructs.ThronLambdaMicroservicePipeline_BuildImageFromDockerfile(scope Construct, repositoryName *string, dockerfilePath *string) IBuildImage
```

###### `scope`<sup>Required</sup> <a name="scope" id="cdk-constructs.ThronLambdaMicroservicePipeline.buildImageFromDockerfile.parameter.scope"></a>

- *Type:* github.com/aws/constructs-go/constructs/v10.Construct

CDK scope to generate the construct in.

---

###### `repositoryName`<sup>Required</sup> <a name="repositoryName" id="cdk-constructs.ThronLambdaMicroservicePipeline.buildImageFromDockerfile.parameter.repositoryName"></a>

- *Type:* *string

Name of the repository that will be created to host the image in.

---

###### `dockerfilePath`<sup>Required</sup> <a name="dockerfilePath" id="cdk-constructs.ThronLambdaMicroservicePipeline.buildImageFromDockerfile.parameter.dockerfilePath"></a>

- *Type:* *string

Path of the docker file to build.

---

##### `BuildImageFromRepository` <a name="BuildImageFromRepository" id="cdk-constructs.ThronLambdaMicroservicePipeline.buildImageFromRepository"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

cdkconstructs.ThronLambdaMicroservicePipeline_BuildImageFromRepository(scope Construct, repositoryName *string, imageTag *string) IBuildImage
```

Constructs a Build Image to be used in the pipeline steps.

###### `scope`<sup>Required</sup> <a name="scope" id="cdk-constructs.ThronLambdaMicroservicePipeline.buildImageFromRepository.parameter.scope"></a>

- *Type:* github.com/aws/constructs-go/constructs/v10.Construct

CDK scope to generate the construct in.

---

###### `repositoryName`<sup>Required</sup> <a name="repositoryName" id="cdk-constructs.ThronLambdaMicroservicePipeline.buildImageFromRepository.parameter.repositoryName"></a>

- *Type:* *string

Name of the private repository to pull the image from.

---

###### `imageTag`<sup>Optional</sup> <a name="imageTag" id="cdk-constructs.ThronLambdaMicroservicePipeline.buildImageFromRepository.parameter.imageTag"></a>

- *Type:* *string

Tag of the image.

Defaults to `latest`

---

#### Properties <a name="Properties" id="Properties"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.ThronLambdaMicroservicePipeline.property.node">Node</a></code> | <code>github.com/aws/constructs-go/constructs/v10.Node</code> | The tree node. |
| <code><a href="#cdk-constructs.ThronLambdaMicroservicePipeline.property.pipelines">Pipelines</a></code> | <code>*map[string]<a href="#cdk-constructs.ThronLambdaSingleEnvPipeline">ThronLambdaSingleEnvPipeline</a></code> | *No description.* |

---

##### `Node`<sup>Required</sup> <a name="Node" id="cdk-constructs.ThronLambdaMicroservicePipeline.property.node"></a>

```go
func Node() Node
```

- *Type:* github.com/aws/constructs-go/constructs/v10.Node

The tree node.

---

##### `Pipelines`<sup>Required</sup> <a name="Pipelines" id="cdk-constructs.ThronLambdaMicroservicePipeline.property.pipelines"></a>

```go
func Pipelines() *map[string]ThronLambdaSingleEnvPipeline
```

- *Type:* *map[string]<a href="#cdk-constructs.ThronLambdaSingleEnvPipeline">ThronLambdaSingleEnvPipeline</a>

---

#### Constants <a name="Constants" id="Constants"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.ThronLambdaMicroservicePipeline.property.DeployConfigs">DeployConfigs</a></code> | <code>*map[string]<a href="#cdk-constructs.EnvironmentConfig">EnvironmentConfig</a></code> | Static and hardcoded deploy configs for the various environments. |

---

##### `DeployConfigs`<sup>Required</sup> <a name="DeployConfigs" id="cdk-constructs.ThronLambdaMicroservicePipeline.property.DeployConfigs"></a>

```go
func DeployConfigs() *map[string]EnvironmentConfig
```

- *Type:* *map[string]<a href="#cdk-constructs.EnvironmentConfig">EnvironmentConfig</a>

Static and hardcoded deploy configs for the various environments.

---

### ThronLambdaSingleEnvPipeline <a name="ThronLambdaSingleEnvPipeline" id="cdk-constructs.ThronLambdaSingleEnvPipeline"></a>

- *Implements:* github.com/aws/aws-cdk-go/awscdk/v2.aws_iam.IGrantable

Class instantiating a pipeline for a single environment.

Depending on its configuration one might

* Enable or disable the `TEST` Stage
* Enable or disable the `BUILD` Stage
* Enable or disable MsTeams Notifications on various pipeline state change. See {@link PipelineCapability} for more
  You should create `ThronLambdaSingleEnvPipeline` instances via the {@link ThronLambdaSingleEnvPipelineBuilder} builder class

#### Initializers <a name="Initializers" id="cdk-constructs.ThronLambdaSingleEnvPipeline.Initializer"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

cdkconstructs.NewThronLambdaSingleEnvPipeline(scope Construct, id *string, props ThronLambdaSingleEnvPipelineProps) ThronLambdaSingleEnvPipeline
```

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.ThronLambdaSingleEnvPipeline.Initializer.parameter.scope">scope</a></code> | <code>github.com/aws/constructs-go/constructs/v10.Construct</code> | *No description.* |
| <code><a href="#cdk-constructs.ThronLambdaSingleEnvPipeline.Initializer.parameter.id">id</a></code> | <code>*string</code> | *No description.* |
| <code><a href="#cdk-constructs.ThronLambdaSingleEnvPipeline.Initializer.parameter.props">props</a></code> | <code><a href="#cdk-constructs.ThronLambdaSingleEnvPipelineProps">ThronLambdaSingleEnvPipelineProps</a></code> | *No description.* |

---

##### `scope`<sup>Required</sup> <a name="scope" id="cdk-constructs.ThronLambdaSingleEnvPipeline.Initializer.parameter.scope"></a>

- *Type:* github.com/aws/constructs-go/constructs/v10.Construct

---

##### `id`<sup>Required</sup> <a name="id" id="cdk-constructs.ThronLambdaSingleEnvPipeline.Initializer.parameter.id"></a>

- *Type:* *string

---

##### `props`<sup>Required</sup> <a name="props" id="cdk-constructs.ThronLambdaSingleEnvPipeline.Initializer.parameter.props"></a>

- *Type:* <a href="#cdk-constructs.ThronLambdaSingleEnvPipelineProps">ThronLambdaSingleEnvPipelineProps</a>

---

#### Methods <a name="Methods" id="Methods"></a>

| **Name** | **Description** |
| --- | --- |
| <code><a href="#cdk-constructs.ThronLambdaSingleEnvPipeline.toString">ToString</a></code> | Returns a string representation of this construct. |
| <code><a href="#cdk-constructs.ThronLambdaSingleEnvPipeline.addNotifyLambda">AddNotifyLambda</a></code> | *No description.* |
| <code><a href="#cdk-constructs.ThronLambdaSingleEnvPipeline.generateBuildSteps">GenerateBuildSteps</a></code> | *No description.* |
| <code><a href="#cdk-constructs.ThronLambdaSingleEnvPipeline.generateDeploySteps">GenerateDeploySteps</a></code> | *No description.* |
| <code><a href="#cdk-constructs.ThronLambdaSingleEnvPipeline.generateTestSteps">GenerateTestSteps</a></code> | *No description.* |

---

##### `ToString` <a name="ToString" id="cdk-constructs.ThronLambdaSingleEnvPipeline.toString"></a>

```go
func ToString() *string
```

Returns a string representation of this construct.

##### `AddNotifyLambda` <a name="AddNotifyLambda" id="cdk-constructs.ThronLambdaSingleEnvPipeline.addNotifyLambda"></a>

```go
func AddNotifyLambda(props ThronLambdaSingleEnvPipelineProps, pipeline Pipeline)
```

###### `props`<sup>Required</sup> <a name="props" id="cdk-constructs.ThronLambdaSingleEnvPipeline.addNotifyLambda.parameter.props"></a>

- *Type:* <a href="#cdk-constructs.ThronLambdaSingleEnvPipelineProps">ThronLambdaSingleEnvPipelineProps</a>

---

###### `pipeline`<sup>Required</sup> <a name="pipeline" id="cdk-constructs.ThronLambdaSingleEnvPipeline.addNotifyLambda.parameter.pipeline"></a>

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_codepipeline.Pipeline

---

##### `GenerateBuildSteps` <a name="GenerateBuildSteps" id="cdk-constructs.ThronLambdaSingleEnvPipeline.generateBuildSteps"></a>

```go
func GenerateBuildSteps(props ThronLambdaSingleEnvPipelineProps, stageName *string) StageProducts
```

###### `props`<sup>Required</sup> <a name="props" id="cdk-constructs.ThronLambdaSingleEnvPipeline.generateBuildSteps.parameter.props"></a>

- *Type:* <a href="#cdk-constructs.ThronLambdaSingleEnvPipelineProps">ThronLambdaSingleEnvPipelineProps</a>

---

###### `stageName`<sup>Required</sup> <a name="stageName" id="cdk-constructs.ThronLambdaSingleEnvPipeline.generateBuildSteps.parameter.stageName"></a>

- *Type:* *string

---

##### `GenerateDeploySteps` <a name="GenerateDeploySteps" id="cdk-constructs.ThronLambdaSingleEnvPipeline.generateDeploySteps"></a>

```go
func GenerateDeploySteps(props ThronLambdaSingleEnvPipelineProps, stageName *string) StageProducts
```

###### `props`<sup>Required</sup> <a name="props" id="cdk-constructs.ThronLambdaSingleEnvPipeline.generateDeploySteps.parameter.props"></a>

- *Type:* <a href="#cdk-constructs.ThronLambdaSingleEnvPipelineProps">ThronLambdaSingleEnvPipelineProps</a>

---

###### `stageName`<sup>Required</sup> <a name="stageName" id="cdk-constructs.ThronLambdaSingleEnvPipeline.generateDeploySteps.parameter.stageName"></a>

- *Type:* *string

---

##### `GenerateTestSteps` <a name="GenerateTestSteps" id="cdk-constructs.ThronLambdaSingleEnvPipeline.generateTestSteps"></a>

```go
func GenerateTestSteps(props ThronLambdaSingleEnvPipelineProps, stageName *string) StageProducts
```

###### `props`<sup>Required</sup> <a name="props" id="cdk-constructs.ThronLambdaSingleEnvPipeline.generateTestSteps.parameter.props"></a>

- *Type:* <a href="#cdk-constructs.ThronLambdaSingleEnvPipelineProps">ThronLambdaSingleEnvPipelineProps</a>

---

###### `stageName`<sup>Required</sup> <a name="stageName" id="cdk-constructs.ThronLambdaSingleEnvPipeline.generateTestSteps.parameter.stageName"></a>

- *Type:* *string

---

#### Static Functions <a name="Static Functions" id="Static Functions"></a>

| **Name** | **Description** |
| --- | --- |
| <code><a href="#cdk-constructs.ThronLambdaSingleEnvPipeline.isConstruct">IsConstruct</a></code> | Checks if `x` is a construct. |

---

##### `IsConstruct` <a name="IsConstruct" id="cdk-constructs.ThronLambdaSingleEnvPipeline.isConstruct"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

cdkconstructs.ThronLambdaSingleEnvPipeline_IsConstruct(x interface{}) *bool
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

- *Type:* interface{}

Any object.

---

#### Properties <a name="Properties" id="Properties"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.ThronLambdaSingleEnvPipeline.property.node">Node</a></code> | <code>github.com/aws/constructs-go/constructs/v10.Node</code> | The tree node. |
| <code><a href="#cdk-constructs.ThronLambdaSingleEnvPipeline.property.grantPrincipal">GrantPrincipal</a></code> | <code>github.com/aws/aws-cdk-go/awscdk/v2.aws_iam.IPrincipal</code> | The principal to grant permissions to. |

---

##### `Node`<sup>Required</sup> <a name="Node" id="cdk-constructs.ThronLambdaSingleEnvPipeline.property.node"></a>

```go
func Node() Node
```

- *Type:* github.com/aws/constructs-go/constructs/v10.Node

The tree node.

---

##### `GrantPrincipal`<sup>Required</sup> <a name="GrantPrincipal" id="cdk-constructs.ThronLambdaSingleEnvPipeline.property.grantPrincipal"></a>

```go
func GrantPrincipal() IPrincipal
```

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_iam.IPrincipal

The principal to grant permissions to.

---


### ThronNewRelicContextInjector <a name="ThronNewRelicContextInjector" id="cdk-constructs.ThronNewRelicContextInjector"></a>

A construct that injects NewRelic configuration into a Lambda function.

#### Initializers <a name="Initializers" id="cdk-constructs.ThronNewRelicContextInjector.Initializer"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

cdkconstructs.NewThronNewRelicContextInjector(scope Construct, id *string, props ThronNewRelicContextInjectorOptions) ThronNewRelicContextInjector
```

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.ThronNewRelicContextInjector.Initializer.parameter.scope">scope</a></code> | <code>github.com/aws/constructs-go/constructs/v10.Construct</code> | - The scope in which this construct is defined. |
| <code><a href="#cdk-constructs.ThronNewRelicContextInjector.Initializer.parameter.id">id</a></code> | <code>*string</code> | - The scoped construct ID. |
| <code><a href="#cdk-constructs.ThronNewRelicContextInjector.Initializer.parameter.props">props</a></code> | <code><a href="#cdk-constructs.ThronNewRelicContextInjectorOptions">ThronNewRelicContextInjectorOptions</a></code> | - The NewRelic configuration options. |

---

##### `scope`<sup>Required</sup> <a name="scope" id="cdk-constructs.ThronNewRelicContextInjector.Initializer.parameter.scope"></a>

- *Type:* github.com/aws/constructs-go/constructs/v10.Construct

The scope in which this construct is defined.

---

##### `id`<sup>Required</sup> <a name="id" id="cdk-constructs.ThronNewRelicContextInjector.Initializer.parameter.id"></a>

- *Type:* *string

The scoped construct ID.

---

##### `props`<sup>Required</sup> <a name="props" id="cdk-constructs.ThronNewRelicContextInjector.Initializer.parameter.props"></a>

- *Type:* <a href="#cdk-constructs.ThronNewRelicContextInjectorOptions">ThronNewRelicContextInjectorOptions</a>

The NewRelic configuration options.

---

#### Methods <a name="Methods" id="Methods"></a>

| **Name** | **Description** |
| --- | --- |
| <code><a href="#cdk-constructs.ThronNewRelicContextInjector.toString">ToString</a></code> | Returns a string representation of this construct. |
| <code><a href="#cdk-constructs.ThronNewRelicContextInjector.injectEnvironment">InjectEnvironment</a></code> | Injects the NewRelic environment variables into the given Lambda function. |

---

##### `ToString` <a name="ToString" id="cdk-constructs.ThronNewRelicContextInjector.toString"></a>

```go
func ToString() *string
```

Returns a string representation of this construct.

##### `InjectEnvironment` <a name="InjectEnvironment" id="cdk-constructs.ThronNewRelicContextInjector.injectEnvironment"></a>

```go
func InjectEnvironment(lambdaFunction Function)
```

Injects the NewRelic environment variables into the given Lambda function.

###### `lambdaFunction`<sup>Required</sup> <a name="lambdaFunction" id="cdk-constructs.ThronNewRelicContextInjector.injectEnvironment.parameter.lambdaFunction"></a>

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_lambda.Function

The Lambda function to inject the environment variables into.

---

#### Static Functions <a name="Static Functions" id="Static Functions"></a>

| **Name** | **Description** |
| --- | --- |
| <code><a href="#cdk-constructs.ThronNewRelicContextInjector.isConstruct">IsConstruct</a></code> | Checks if `x` is a construct. |

---

##### `IsConstruct` <a name="IsConstruct" id="cdk-constructs.ThronNewRelicContextInjector.isConstruct"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

cdkconstructs.ThronNewRelicContextInjector_IsConstruct(x interface{}) *bool
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

- *Type:* interface{}

Any object.

---

#### Properties <a name="Properties" id="Properties"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.ThronNewRelicContextInjector.property.node">Node</a></code> | <code>github.com/aws/constructs-go/constructs/v10.Node</code> | The tree node. |
| <code><a href="#cdk-constructs.ThronNewRelicContextInjector.property.newRelicEnvironment">NewRelicEnvironment</a></code> | <code>*map[string]*string</code> | *No description.* |

---

##### `Node`<sup>Required</sup> <a name="Node" id="cdk-constructs.ThronNewRelicContextInjector.property.node"></a>

```go
func Node() Node
```

- *Type:* github.com/aws/constructs-go/constructs/v10.Node

The tree node.

---

##### `NewRelicEnvironment`<sup>Required</sup> <a name="NewRelicEnvironment" id="cdk-constructs.ThronNewRelicContextInjector.property.newRelicEnvironment"></a>

```go
func NewRelicEnvironment() *map[string]*string
```

- *Type:* *map[string]*string

---


### ThronNewRelicDockerLambda <a name="ThronNewRelicDockerLambda" id="cdk-constructs.ThronNewRelicDockerLambda"></a>

A Lambda Docker function with NewRelic integration.

#### Initializers <a name="Initializers" id="cdk-constructs.ThronNewRelicDockerLambda.Initializer"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

cdkconstructs.NewThronNewRelicDockerLambda(scope Stack, id *string, props NewRelicFunctionOptions) ThronNewRelicDockerLambda
```

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.ThronNewRelicDockerLambda.Initializer.parameter.scope">scope</a></code> | <code>github.com/aws/aws-cdk-go/awscdk/v2.Stack</code> | - The scope in which this construct is defined. |
| <code><a href="#cdk-constructs.ThronNewRelicDockerLambda.Initializer.parameter.id">id</a></code> | <code>*string</code> | - The scoped construct ID. |
| <code><a href="#cdk-constructs.ThronNewRelicDockerLambda.Initializer.parameter.props">props</a></code> | <code><a href="#cdk-constructs.NewRelicFunctionOptions">NewRelicFunctionOptions</a></code> | - The function properties including NewRelic configuration overrides. |

---

##### `scope`<sup>Required</sup> <a name="scope" id="cdk-constructs.ThronNewRelicDockerLambda.Initializer.parameter.scope"></a>

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.Stack

The scope in which this construct is defined.

---

##### `id`<sup>Required</sup> <a name="id" id="cdk-constructs.ThronNewRelicDockerLambda.Initializer.parameter.id"></a>

- *Type:* *string

The scoped construct ID.

---

##### `props`<sup>Required</sup> <a name="props" id="cdk-constructs.ThronNewRelicDockerLambda.Initializer.parameter.props"></a>

- *Type:* <a href="#cdk-constructs.NewRelicFunctionOptions">NewRelicFunctionOptions</a>

The function properties including NewRelic configuration overrides.

---

#### Methods <a name="Methods" id="Methods"></a>

| **Name** | **Description** |
| --- | --- |
| <code><a href="#cdk-constructs.ThronNewRelicDockerLambda.toString">ToString</a></code> | Returns a string representation of this construct. |
| <code><a href="#cdk-constructs.ThronNewRelicDockerLambda.applyRemovalPolicy">ApplyRemovalPolicy</a></code> | Apply the given removal policy to this resource. |
| <code><a href="#cdk-constructs.ThronNewRelicDockerLambda.addEventSource">AddEventSource</a></code> | Adds an event source to this function. |
| <code><a href="#cdk-constructs.ThronNewRelicDockerLambda.addEventSourceMapping">AddEventSourceMapping</a></code> | Adds an event source that maps to this AWS Lambda function. |
| <code><a href="#cdk-constructs.ThronNewRelicDockerLambda.addFunctionUrl">AddFunctionUrl</a></code> | Adds a url to this lambda function. |
| <code><a href="#cdk-constructs.ThronNewRelicDockerLambda.addPermission">AddPermission</a></code> | Adds a permission to the Lambda resource policy. |
| <code><a href="#cdk-constructs.ThronNewRelicDockerLambda.addToRolePolicy">AddToRolePolicy</a></code> | Adds a statement to the IAM role assumed by the instance. |
| <code><a href="#cdk-constructs.ThronNewRelicDockerLambda.configureAsyncInvoke">ConfigureAsyncInvoke</a></code> | Configures options for asynchronous invocation. |
| <code><a href="#cdk-constructs.ThronNewRelicDockerLambda.considerWarningOnInvokeFunctionPermissions">ConsiderWarningOnInvokeFunctionPermissions</a></code> | A warning will be added to functions under the following conditions: - permissions that include `lambda:InvokeFunction` are added to the unqualified function. |
| <code><a href="#cdk-constructs.ThronNewRelicDockerLambda.grantInvoke">GrantInvoke</a></code> | Grant the given identity permissions to invoke this Lambda. |
| <code><a href="#cdk-constructs.ThronNewRelicDockerLambda.grantInvokeCompositePrincipal">GrantInvokeCompositePrincipal</a></code> | Grant multiple principals the ability to invoke this Lambda via CompositePrincipal. |
| <code><a href="#cdk-constructs.ThronNewRelicDockerLambda.grantInvokeLatestVersion">GrantInvokeLatestVersion</a></code> | Grant the given identity permissions to invoke the $LATEST version or unqualified version of this Lambda. |
| <code><a href="#cdk-constructs.ThronNewRelicDockerLambda.grantInvokeUrl">GrantInvokeUrl</a></code> | Grant the given identity permissions to invoke this Lambda Function URL. |
| <code><a href="#cdk-constructs.ThronNewRelicDockerLambda.grantInvokeVersion">GrantInvokeVersion</a></code> | Grant the given identity permissions to invoke the given version of this Lambda. |
| <code><a href="#cdk-constructs.ThronNewRelicDockerLambda.metric">Metric</a></code> | Return the given named metric for this Function. |
| <code><a href="#cdk-constructs.ThronNewRelicDockerLambda.metricDuration">MetricDuration</a></code> | How long execution of this Lambda takes. |
| <code><a href="#cdk-constructs.ThronNewRelicDockerLambda.metricErrors">MetricErrors</a></code> | How many invocations of this Lambda fail. |
| <code><a href="#cdk-constructs.ThronNewRelicDockerLambda.metricInvocations">MetricInvocations</a></code> | How often this Lambda is invoked. |
| <code><a href="#cdk-constructs.ThronNewRelicDockerLambda.metricThrottles">MetricThrottles</a></code> | How often this Lambda is throttled. |
| <code><a href="#cdk-constructs.ThronNewRelicDockerLambda.addAlias">AddAlias</a></code> | Defines an alias for this function. |
| <code><a href="#cdk-constructs.ThronNewRelicDockerLambda.addEnvironment">AddEnvironment</a></code> | Adds an environment variable to this Lambda function. |
| <code><a href="#cdk-constructs.ThronNewRelicDockerLambda.addLayers">AddLayers</a></code> | Adds one or more Lambda Layers to this Lambda function. |
| <code><a href="#cdk-constructs.ThronNewRelicDockerLambda.invalidateVersionBasedOn">InvalidateVersionBasedOn</a></code> | Mix additional information into the hash of the Version object. |
| <code><a href="#cdk-constructs.ThronNewRelicDockerLambda.addEndpointAlb">AddEndpointAlb</a></code> | Add an endpoint the lambda function. |
| <code><a href="#cdk-constructs.ThronNewRelicDockerLambda.addLegacyEndpointAlb">AddLegacyEndpointAlb</a></code> | Add a legacy endpoint to the lambda function. |

---

##### `ToString` <a name="ToString" id="cdk-constructs.ThronNewRelicDockerLambda.toString"></a>

```go
func ToString() *string
```

Returns a string representation of this construct.

##### `ApplyRemovalPolicy` <a name="ApplyRemovalPolicy" id="cdk-constructs.ThronNewRelicDockerLambda.applyRemovalPolicy"></a>

```go
func ApplyRemovalPolicy(policy RemovalPolicy)
```

Apply the given removal policy to this resource.

The Removal Policy controls what happens to this resource when it stops
being managed by CloudFormation, either because you've removed it from the
CDK application or because you've made a change that requires the resource
to be replaced.

The resource can be deleted (`RemovalPolicy.DESTROY`), or left in your AWS
account for data recovery and cleanup later (`RemovalPolicy.RETAIN`).

###### `policy`<sup>Required</sup> <a name="policy" id="cdk-constructs.ThronNewRelicDockerLambda.applyRemovalPolicy.parameter.policy"></a>

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.RemovalPolicy

---

##### `AddEventSource` <a name="AddEventSource" id="cdk-constructs.ThronNewRelicDockerLambda.addEventSource"></a>

```go
func AddEventSource(source IEventSource)
```

Adds an event source to this function.

Event sources are implemented in the aws-cdk-lib/aws-lambda-event-sources module.

The following example adds an SQS Queue as an event source:
```
import { SqsEventSource } from 'aws-cdk-lib/aws-lambda-event-sources';
myFunction.addEventSource(new SqsEventSource(myQueue));
```

###### `source`<sup>Required</sup> <a name="source" id="cdk-constructs.ThronNewRelicDockerLambda.addEventSource.parameter.source"></a>

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_lambda.IEventSource

---

##### `AddEventSourceMapping` <a name="AddEventSourceMapping" id="cdk-constructs.ThronNewRelicDockerLambda.addEventSourceMapping"></a>

```go
func AddEventSourceMapping(id *string, options EventSourceMappingOptions) EventSourceMapping
```

Adds an event source that maps to this AWS Lambda function.

###### `id`<sup>Required</sup> <a name="id" id="cdk-constructs.ThronNewRelicDockerLambda.addEventSourceMapping.parameter.id"></a>

- *Type:* *string

---

###### `options`<sup>Required</sup> <a name="options" id="cdk-constructs.ThronNewRelicDockerLambda.addEventSourceMapping.parameter.options"></a>

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_lambda.EventSourceMappingOptions

---

##### `AddFunctionUrl` <a name="AddFunctionUrl" id="cdk-constructs.ThronNewRelicDockerLambda.addFunctionUrl"></a>

```go
func AddFunctionUrl(options FunctionUrlOptions) FunctionUrl
```

Adds a url to this lambda function.

###### `options`<sup>Optional</sup> <a name="options" id="cdk-constructs.ThronNewRelicDockerLambda.addFunctionUrl.parameter.options"></a>

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_lambda.FunctionUrlOptions

---

##### `AddPermission` <a name="AddPermission" id="cdk-constructs.ThronNewRelicDockerLambda.addPermission"></a>

```go
func AddPermission(id *string, permission Permission)
```

Adds a permission to the Lambda resource policy.

> [Permission for details.](Permission for details.)

###### `id`<sup>Required</sup> <a name="id" id="cdk-constructs.ThronNewRelicDockerLambda.addPermission.parameter.id"></a>

- *Type:* *string

The id for the permission construct.

---

###### `permission`<sup>Required</sup> <a name="permission" id="cdk-constructs.ThronNewRelicDockerLambda.addPermission.parameter.permission"></a>

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_lambda.Permission

The permission to grant to this Lambda function.

---

##### `AddToRolePolicy` <a name="AddToRolePolicy" id="cdk-constructs.ThronNewRelicDockerLambda.addToRolePolicy"></a>

```go
func AddToRolePolicy(statement PolicyStatement)
```

Adds a statement to the IAM role assumed by the instance.

###### `statement`<sup>Required</sup> <a name="statement" id="cdk-constructs.ThronNewRelicDockerLambda.addToRolePolicy.parameter.statement"></a>

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_iam.PolicyStatement

---

##### `ConfigureAsyncInvoke` <a name="ConfigureAsyncInvoke" id="cdk-constructs.ThronNewRelicDockerLambda.configureAsyncInvoke"></a>

```go
func ConfigureAsyncInvoke(options EventInvokeConfigOptions)
```

Configures options for asynchronous invocation.

###### `options`<sup>Required</sup> <a name="options" id="cdk-constructs.ThronNewRelicDockerLambda.configureAsyncInvoke.parameter.options"></a>

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_lambda.EventInvokeConfigOptions

---

##### `ConsiderWarningOnInvokeFunctionPermissions` <a name="ConsiderWarningOnInvokeFunctionPermissions" id="cdk-constructs.ThronNewRelicDockerLambda.considerWarningOnInvokeFunctionPermissions"></a>

```go
func ConsiderWarningOnInvokeFunctionPermissions(scope Construct, action *string)
```

A warning will be added to functions under the following conditions: - permissions that include `lambda:InvokeFunction` are added to the unqualified function.

function.currentVersion is invoked before or after the permission is created.

This applies only to permissions on Lambda functions, not versions or aliases.
This function is overridden as a noOp for QualifiedFunctionBase.

###### `scope`<sup>Required</sup> <a name="scope" id="cdk-constructs.ThronNewRelicDockerLambda.considerWarningOnInvokeFunctionPermissions.parameter.scope"></a>

- *Type:* github.com/aws/constructs-go/constructs/v10.Construct

---

###### `action`<sup>Required</sup> <a name="action" id="cdk-constructs.ThronNewRelicDockerLambda.considerWarningOnInvokeFunctionPermissions.parameter.action"></a>

- *Type:* *string

---

##### `GrantInvoke` <a name="GrantInvoke" id="cdk-constructs.ThronNewRelicDockerLambda.grantInvoke"></a>

```go
func GrantInvoke(grantee IGrantable) Grant
```

Grant the given identity permissions to invoke this Lambda.

###### `grantee`<sup>Required</sup> <a name="grantee" id="cdk-constructs.ThronNewRelicDockerLambda.grantInvoke.parameter.grantee"></a>

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_iam.IGrantable

---

##### `GrantInvokeCompositePrincipal` <a name="GrantInvokeCompositePrincipal" id="cdk-constructs.ThronNewRelicDockerLambda.grantInvokeCompositePrincipal"></a>

```go
func GrantInvokeCompositePrincipal(compositePrincipal CompositePrincipal) *[]Grant
```

Grant multiple principals the ability to invoke this Lambda via CompositePrincipal.

###### `compositePrincipal`<sup>Required</sup> <a name="compositePrincipal" id="cdk-constructs.ThronNewRelicDockerLambda.grantInvokeCompositePrincipal.parameter.compositePrincipal"></a>

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_iam.CompositePrincipal

---

##### `GrantInvokeLatestVersion` <a name="GrantInvokeLatestVersion" id="cdk-constructs.ThronNewRelicDockerLambda.grantInvokeLatestVersion"></a>

```go
func GrantInvokeLatestVersion(grantee IGrantable) Grant
```

Grant the given identity permissions to invoke the $LATEST version or unqualified version of this Lambda.

###### `grantee`<sup>Required</sup> <a name="grantee" id="cdk-constructs.ThronNewRelicDockerLambda.grantInvokeLatestVersion.parameter.grantee"></a>

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_iam.IGrantable

---

##### `GrantInvokeUrl` <a name="GrantInvokeUrl" id="cdk-constructs.ThronNewRelicDockerLambda.grantInvokeUrl"></a>

```go
func GrantInvokeUrl(grantee IGrantable) Grant
```

Grant the given identity permissions to invoke this Lambda Function URL.

###### `grantee`<sup>Required</sup> <a name="grantee" id="cdk-constructs.ThronNewRelicDockerLambda.grantInvokeUrl.parameter.grantee"></a>

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_iam.IGrantable

---

##### `GrantInvokeVersion` <a name="GrantInvokeVersion" id="cdk-constructs.ThronNewRelicDockerLambda.grantInvokeVersion"></a>

```go
func GrantInvokeVersion(grantee IGrantable, version IVersion) Grant
```

Grant the given identity permissions to invoke the given version of this Lambda.

###### `grantee`<sup>Required</sup> <a name="grantee" id="cdk-constructs.ThronNewRelicDockerLambda.grantInvokeVersion.parameter.grantee"></a>

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_iam.IGrantable

---

###### `version`<sup>Required</sup> <a name="version" id="cdk-constructs.ThronNewRelicDockerLambda.grantInvokeVersion.parameter.version"></a>

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_lambda.IVersion

---

##### `Metric` <a name="Metric" id="cdk-constructs.ThronNewRelicDockerLambda.metric"></a>

```go
func Metric(metricName *string, props MetricOptions) Metric
```

Return the given named metric for this Function.

###### `metricName`<sup>Required</sup> <a name="metricName" id="cdk-constructs.ThronNewRelicDockerLambda.metric.parameter.metricName"></a>

- *Type:* *string

---

###### `props`<sup>Optional</sup> <a name="props" id="cdk-constructs.ThronNewRelicDockerLambda.metric.parameter.props"></a>

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_cloudwatch.MetricOptions

---

##### `MetricDuration` <a name="MetricDuration" id="cdk-constructs.ThronNewRelicDockerLambda.metricDuration"></a>

```go
func MetricDuration(props MetricOptions) Metric
```

How long execution of this Lambda takes.

Average over 5 minutes

###### `props`<sup>Optional</sup> <a name="props" id="cdk-constructs.ThronNewRelicDockerLambda.metricDuration.parameter.props"></a>

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_cloudwatch.MetricOptions

---

##### `MetricErrors` <a name="MetricErrors" id="cdk-constructs.ThronNewRelicDockerLambda.metricErrors"></a>

```go
func MetricErrors(props MetricOptions) Metric
```

How many invocations of this Lambda fail.

Sum over 5 minutes

###### `props`<sup>Optional</sup> <a name="props" id="cdk-constructs.ThronNewRelicDockerLambda.metricErrors.parameter.props"></a>

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_cloudwatch.MetricOptions

---

##### `MetricInvocations` <a name="MetricInvocations" id="cdk-constructs.ThronNewRelicDockerLambda.metricInvocations"></a>

```go
func MetricInvocations(props MetricOptions) Metric
```

How often this Lambda is invoked.

Sum over 5 minutes

###### `props`<sup>Optional</sup> <a name="props" id="cdk-constructs.ThronNewRelicDockerLambda.metricInvocations.parameter.props"></a>

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_cloudwatch.MetricOptions

---

##### `MetricThrottles` <a name="MetricThrottles" id="cdk-constructs.ThronNewRelicDockerLambda.metricThrottles"></a>

```go
func MetricThrottles(props MetricOptions) Metric
```

How often this Lambda is throttled.

Sum over 5 minutes

###### `props`<sup>Optional</sup> <a name="props" id="cdk-constructs.ThronNewRelicDockerLambda.metricThrottles.parameter.props"></a>

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_cloudwatch.MetricOptions

---

##### `AddAlias` <a name="AddAlias" id="cdk-constructs.ThronNewRelicDockerLambda.addAlias"></a>

```go
func AddAlias(aliasName *string, options AliasOptions) Alias
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

- *Type:* *string

The name of the alias.

---

###### `options`<sup>Optional</sup> <a name="options" id="cdk-constructs.ThronNewRelicDockerLambda.addAlias.parameter.options"></a>

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_lambda.AliasOptions

Alias options.

---

##### `AddEnvironment` <a name="AddEnvironment" id="cdk-constructs.ThronNewRelicDockerLambda.addEnvironment"></a>

```go
func AddEnvironment(key *string, value *string, options EnvironmentOptions) Function
```

Adds an environment variable to this Lambda function.

If this is a ref to a Lambda function, this operation results in a no-op.

###### `key`<sup>Required</sup> <a name="key" id="cdk-constructs.ThronNewRelicDockerLambda.addEnvironment.parameter.key"></a>

- *Type:* *string

The environment variable key.

---

###### `value`<sup>Required</sup> <a name="value" id="cdk-constructs.ThronNewRelicDockerLambda.addEnvironment.parameter.value"></a>

- *Type:* *string

The environment variable's value.

---

###### `options`<sup>Optional</sup> <a name="options" id="cdk-constructs.ThronNewRelicDockerLambda.addEnvironment.parameter.options"></a>

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_lambda.EnvironmentOptions

Environment variable options.

---

##### `AddLayers` <a name="AddLayers" id="cdk-constructs.ThronNewRelicDockerLambda.addLayers"></a>

```go
func AddLayers(layers ILayerVersion)
```

Adds one or more Lambda Layers to this Lambda function.

###### `layers`<sup>Required</sup> <a name="layers" id="cdk-constructs.ThronNewRelicDockerLambda.addLayers.parameter.layers"></a>

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_lambda.ILayerVersion

the layers to be added.

---

##### `InvalidateVersionBasedOn` <a name="InvalidateVersionBasedOn" id="cdk-constructs.ThronNewRelicDockerLambda.invalidateVersionBasedOn"></a>

```go
func InvalidateVersionBasedOn(x *string)
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

- *Type:* *string

---

##### `AddEndpointAlb` <a name="AddEndpointAlb" id="cdk-constructs.ThronNewRelicDockerLambda.addEndpointAlb"></a>

```go
func AddEndpointAlb(name *string, endpointProps ThronEndpointAlbProps) EndpointAlb
```

Add an endpoint the lambda function.

###### `name`<sup>Required</sup> <a name="name" id="cdk-constructs.ThronNewRelicDockerLambda.addEndpointAlb.parameter.name"></a>

- *Type:* *string

---

###### `endpointProps`<sup>Required</sup> <a name="endpointProps" id="cdk-constructs.ThronNewRelicDockerLambda.addEndpointAlb.parameter.endpointProps"></a>

- *Type:* <a href="#cdk-constructs.ThronEndpointAlbProps">ThronEndpointAlbProps</a>

---

##### `AddLegacyEndpointAlb` <a name="AddLegacyEndpointAlb" id="cdk-constructs.ThronNewRelicDockerLambda.addLegacyEndpointAlb"></a>

```go
func AddLegacyEndpointAlb(name *string, endpointProps LegacyEndpointAlbProps) EndpointAlb
```

Add a legacy endpoint to the lambda function.

###### `name`<sup>Required</sup> <a name="name" id="cdk-constructs.ThronNewRelicDockerLambda.addLegacyEndpointAlb.parameter.name"></a>

- *Type:* *string

---

###### `endpointProps`<sup>Required</sup> <a name="endpointProps" id="cdk-constructs.ThronNewRelicDockerLambda.addLegacyEndpointAlb.parameter.endpointProps"></a>

- *Type:* <a href="#cdk-constructs.LegacyEndpointAlbProps">LegacyEndpointAlbProps</a>

---

#### Static Functions <a name="Static Functions" id="Static Functions"></a>

| **Name** | **Description** |
| --- | --- |
| <code><a href="#cdk-constructs.ThronNewRelicDockerLambda.isConstruct">IsConstruct</a></code> | Checks if `x` is a construct. |
| <code><a href="#cdk-constructs.ThronNewRelicDockerLambda.isOwnedResource">IsOwnedResource</a></code> | Returns true if the construct was created by CDK, and false otherwise. |
| <code><a href="#cdk-constructs.ThronNewRelicDockerLambda.isResource">IsResource</a></code> | Check whether the given construct is a Resource. |
| <code><a href="#cdk-constructs.ThronNewRelicDockerLambda.classifyVersionProperty">ClassifyVersionProperty</a></code> | Record whether specific properties in the `AWS::Lambda::Function` resource should also be associated to the Version resource. |
| <code><a href="#cdk-constructs.ThronNewRelicDockerLambda.fromFunctionArn">FromFunctionArn</a></code> | Import a lambda function into the CDK using its ARN. |
| <code><a href="#cdk-constructs.ThronNewRelicDockerLambda.fromFunctionAttributes">FromFunctionAttributes</a></code> | Creates a Lambda function object which represents a function not defined within this stack. |
| <code><a href="#cdk-constructs.ThronNewRelicDockerLambda.fromFunctionName">FromFunctionName</a></code> | Import a lambda function into the CDK using its name. |
| <code><a href="#cdk-constructs.ThronNewRelicDockerLambda.metricAll">MetricAll</a></code> | Return the given named metric for this Lambda. |
| <code><a href="#cdk-constructs.ThronNewRelicDockerLambda.metricAllConcurrentExecutions">MetricAllConcurrentExecutions</a></code> | Metric for the number of concurrent executions across all Lambdas. |
| <code><a href="#cdk-constructs.ThronNewRelicDockerLambda.metricAllDuration">MetricAllDuration</a></code> | Metric for the Duration executing all Lambdas. |
| <code><a href="#cdk-constructs.ThronNewRelicDockerLambda.metricAllErrors">MetricAllErrors</a></code> | Metric for the number of Errors executing all Lambdas. |
| <code><a href="#cdk-constructs.ThronNewRelicDockerLambda.metricAllInvocations">MetricAllInvocations</a></code> | Metric for the number of invocations of all Lambdas. |
| <code><a href="#cdk-constructs.ThronNewRelicDockerLambda.metricAllThrottles">MetricAllThrottles</a></code> | Metric for the number of throttled invocations of all Lambdas. |
| <code><a href="#cdk-constructs.ThronNewRelicDockerLambda.metricAllUnreservedConcurrentExecutions">MetricAllUnreservedConcurrentExecutions</a></code> | Metric for the number of unreserved concurrent executions across all Lambdas. |

---

##### `IsConstruct` <a name="IsConstruct" id="cdk-constructs.ThronNewRelicDockerLambda.isConstruct"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

cdkconstructs.ThronNewRelicDockerLambda_IsConstruct(x interface{}) *bool
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

- *Type:* interface{}

Any object.

---

##### `IsOwnedResource` <a name="IsOwnedResource" id="cdk-constructs.ThronNewRelicDockerLambda.isOwnedResource"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

cdkconstructs.ThronNewRelicDockerLambda_IsOwnedResource(construct IConstruct) *bool
```

Returns true if the construct was created by CDK, and false otherwise.

###### `construct`<sup>Required</sup> <a name="construct" id="cdk-constructs.ThronNewRelicDockerLambda.isOwnedResource.parameter.construct"></a>

- *Type:* github.com/aws/constructs-go/constructs/v10.IConstruct

---

##### `IsResource` <a name="IsResource" id="cdk-constructs.ThronNewRelicDockerLambda.isResource"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

cdkconstructs.ThronNewRelicDockerLambda_IsResource(construct IConstruct) *bool
```

Check whether the given construct is a Resource.

###### `construct`<sup>Required</sup> <a name="construct" id="cdk-constructs.ThronNewRelicDockerLambda.isResource.parameter.construct"></a>

- *Type:* github.com/aws/constructs-go/constructs/v10.IConstruct

---

##### `ClassifyVersionProperty` <a name="ClassifyVersionProperty" id="cdk-constructs.ThronNewRelicDockerLambda.classifyVersionProperty"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

cdkconstructs.ThronNewRelicDockerLambda_ClassifyVersionProperty(propertyName *string, locked *bool)
```

Record whether specific properties in the `AWS::Lambda::Function` resource should also be associated to the Version resource.

See 'currentVersion' section in the module README for more details.

###### `propertyName`<sup>Required</sup> <a name="propertyName" id="cdk-constructs.ThronNewRelicDockerLambda.classifyVersionProperty.parameter.propertyName"></a>

- *Type:* *string

The property to classify.

---

###### `locked`<sup>Required</sup> <a name="locked" id="cdk-constructs.ThronNewRelicDockerLambda.classifyVersionProperty.parameter.locked"></a>

- *Type:* *bool

whether the property should be associated to the version or not.

---

##### `FromFunctionArn` <a name="FromFunctionArn" id="cdk-constructs.ThronNewRelicDockerLambda.fromFunctionArn"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

cdkconstructs.ThronNewRelicDockerLambda_FromFunctionArn(scope Construct, id *string, functionArn *string) IFunction
```

Import a lambda function into the CDK using its ARN.

For `Function.addPermissions()` to work on this imported lambda, make sure that is
in the same account and region as the stack you are importing it into.

###### `scope`<sup>Required</sup> <a name="scope" id="cdk-constructs.ThronNewRelicDockerLambda.fromFunctionArn.parameter.scope"></a>

- *Type:* github.com/aws/constructs-go/constructs/v10.Construct

---

###### `id`<sup>Required</sup> <a name="id" id="cdk-constructs.ThronNewRelicDockerLambda.fromFunctionArn.parameter.id"></a>

- *Type:* *string

---

###### `functionArn`<sup>Required</sup> <a name="functionArn" id="cdk-constructs.ThronNewRelicDockerLambda.fromFunctionArn.parameter.functionArn"></a>

- *Type:* *string

---

##### `FromFunctionAttributes` <a name="FromFunctionAttributes" id="cdk-constructs.ThronNewRelicDockerLambda.fromFunctionAttributes"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

cdkconstructs.ThronNewRelicDockerLambda_FromFunctionAttributes(scope Construct, id *string, attrs FunctionAttributes) IFunction
```

Creates a Lambda function object which represents a function not defined within this stack.

For `Function.addPermissions()` to work on this imported lambda, set the sameEnvironment property to true
if this imported lambda is in the same account and region as the stack you are importing it into.

###### `scope`<sup>Required</sup> <a name="scope" id="cdk-constructs.ThronNewRelicDockerLambda.fromFunctionAttributes.parameter.scope"></a>

- *Type:* github.com/aws/constructs-go/constructs/v10.Construct

The parent construct.

---

###### `id`<sup>Required</sup> <a name="id" id="cdk-constructs.ThronNewRelicDockerLambda.fromFunctionAttributes.parameter.id"></a>

- *Type:* *string

The name of the lambda construct.

---

###### `attrs`<sup>Required</sup> <a name="attrs" id="cdk-constructs.ThronNewRelicDockerLambda.fromFunctionAttributes.parameter.attrs"></a>

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_lambda.FunctionAttributes

the attributes of the function to import.

---

##### `FromFunctionName` <a name="FromFunctionName" id="cdk-constructs.ThronNewRelicDockerLambda.fromFunctionName"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

cdkconstructs.ThronNewRelicDockerLambda_FromFunctionName(scope Construct, id *string, functionName *string) IFunction
```

Import a lambda function into the CDK using its name.

###### `scope`<sup>Required</sup> <a name="scope" id="cdk-constructs.ThronNewRelicDockerLambda.fromFunctionName.parameter.scope"></a>

- *Type:* github.com/aws/constructs-go/constructs/v10.Construct

---

###### `id`<sup>Required</sup> <a name="id" id="cdk-constructs.ThronNewRelicDockerLambda.fromFunctionName.parameter.id"></a>

- *Type:* *string

---

###### `functionName`<sup>Required</sup> <a name="functionName" id="cdk-constructs.ThronNewRelicDockerLambda.fromFunctionName.parameter.functionName"></a>

- *Type:* *string

---

##### `MetricAll` <a name="MetricAll" id="cdk-constructs.ThronNewRelicDockerLambda.metricAll"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

cdkconstructs.ThronNewRelicDockerLambda_MetricAll(metricName *string, props MetricOptions) Metric
```

Return the given named metric for this Lambda.

###### `metricName`<sup>Required</sup> <a name="metricName" id="cdk-constructs.ThronNewRelicDockerLambda.metricAll.parameter.metricName"></a>

- *Type:* *string

---

###### `props`<sup>Optional</sup> <a name="props" id="cdk-constructs.ThronNewRelicDockerLambda.metricAll.parameter.props"></a>

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_cloudwatch.MetricOptions

---

##### `MetricAllConcurrentExecutions` <a name="MetricAllConcurrentExecutions" id="cdk-constructs.ThronNewRelicDockerLambda.metricAllConcurrentExecutions"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

cdkconstructs.ThronNewRelicDockerLambda_MetricAllConcurrentExecutions(props MetricOptions) Metric
```

Metric for the number of concurrent executions across all Lambdas.

###### `props`<sup>Optional</sup> <a name="props" id="cdk-constructs.ThronNewRelicDockerLambda.metricAllConcurrentExecutions.parameter.props"></a>

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_cloudwatch.MetricOptions

---

##### `MetricAllDuration` <a name="MetricAllDuration" id="cdk-constructs.ThronNewRelicDockerLambda.metricAllDuration"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

cdkconstructs.ThronNewRelicDockerLambda_MetricAllDuration(props MetricOptions) Metric
```

Metric for the Duration executing all Lambdas.

###### `props`<sup>Optional</sup> <a name="props" id="cdk-constructs.ThronNewRelicDockerLambda.metricAllDuration.parameter.props"></a>

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_cloudwatch.MetricOptions

---

##### `MetricAllErrors` <a name="MetricAllErrors" id="cdk-constructs.ThronNewRelicDockerLambda.metricAllErrors"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

cdkconstructs.ThronNewRelicDockerLambda_MetricAllErrors(props MetricOptions) Metric
```

Metric for the number of Errors executing all Lambdas.

###### `props`<sup>Optional</sup> <a name="props" id="cdk-constructs.ThronNewRelicDockerLambda.metricAllErrors.parameter.props"></a>

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_cloudwatch.MetricOptions

---

##### `MetricAllInvocations` <a name="MetricAllInvocations" id="cdk-constructs.ThronNewRelicDockerLambda.metricAllInvocations"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

cdkconstructs.ThronNewRelicDockerLambda_MetricAllInvocations(props MetricOptions) Metric
```

Metric for the number of invocations of all Lambdas.

###### `props`<sup>Optional</sup> <a name="props" id="cdk-constructs.ThronNewRelicDockerLambda.metricAllInvocations.parameter.props"></a>

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_cloudwatch.MetricOptions

---

##### `MetricAllThrottles` <a name="MetricAllThrottles" id="cdk-constructs.ThronNewRelicDockerLambda.metricAllThrottles"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

cdkconstructs.ThronNewRelicDockerLambda_MetricAllThrottles(props MetricOptions) Metric
```

Metric for the number of throttled invocations of all Lambdas.

###### `props`<sup>Optional</sup> <a name="props" id="cdk-constructs.ThronNewRelicDockerLambda.metricAllThrottles.parameter.props"></a>

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_cloudwatch.MetricOptions

---

##### `MetricAllUnreservedConcurrentExecutions` <a name="MetricAllUnreservedConcurrentExecutions" id="cdk-constructs.ThronNewRelicDockerLambda.metricAllUnreservedConcurrentExecutions"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

cdkconstructs.ThronNewRelicDockerLambda_MetricAllUnreservedConcurrentExecutions(props MetricOptions) Metric
```

Metric for the number of unreserved concurrent executions across all Lambdas.

###### `props`<sup>Optional</sup> <a name="props" id="cdk-constructs.ThronNewRelicDockerLambda.metricAllUnreservedConcurrentExecutions.parameter.props"></a>

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_cloudwatch.MetricOptions

---

#### Properties <a name="Properties" id="Properties"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.ThronNewRelicDockerLambda.property.node">Node</a></code> | <code>github.com/aws/constructs-go/constructs/v10.Node</code> | The tree node. |
| <code><a href="#cdk-constructs.ThronNewRelicDockerLambda.property.env">Env</a></code> | <code>github.com/aws/aws-cdk-go/awscdk/v2.ResourceEnvironment</code> | The environment this resource belongs to. |
| <code><a href="#cdk-constructs.ThronNewRelicDockerLambda.property.stack">Stack</a></code> | <code>github.com/aws/aws-cdk-go/awscdk/v2.Stack</code> | The stack in which this resource is defined. |
| <code><a href="#cdk-constructs.ThronNewRelicDockerLambda.property.architecture">Architecture</a></code> | <code>github.com/aws/aws-cdk-go/awscdk/v2.aws_lambda.Architecture</code> | The architecture of this Lambda Function (this is an optional attribute and defaults to X86_64). |
| <code><a href="#cdk-constructs.ThronNewRelicDockerLambda.property.connections">Connections</a></code> | <code>github.com/aws/aws-cdk-go/awscdk/v2.aws_ec2.Connections</code> | Access the Connections object. |
| <code><a href="#cdk-constructs.ThronNewRelicDockerLambda.property.functionArn">FunctionArn</a></code> | <code>*string</code> | ARN of this function. |
| <code><a href="#cdk-constructs.ThronNewRelicDockerLambda.property.functionName">FunctionName</a></code> | <code>*string</code> | Name of this function. |
| <code><a href="#cdk-constructs.ThronNewRelicDockerLambda.property.grantPrincipal">GrantPrincipal</a></code> | <code>github.com/aws/aws-cdk-go/awscdk/v2.aws_iam.IPrincipal</code> | The principal this Lambda Function is running as. |
| <code><a href="#cdk-constructs.ThronNewRelicDockerLambda.property.isBoundToVpc">IsBoundToVpc</a></code> | <code>*bool</code> | Whether or not this Lambda function was bound to a VPC. |
| <code><a href="#cdk-constructs.ThronNewRelicDockerLambda.property.latestVersion">LatestVersion</a></code> | <code>github.com/aws/aws-cdk-go/awscdk/v2.aws_lambda.IVersion</code> | The `$LATEST` version of this function. |
| <code><a href="#cdk-constructs.ThronNewRelicDockerLambda.property.permissionsNode">PermissionsNode</a></code> | <code>github.com/aws/constructs-go/constructs/v10.Node</code> | The construct node where permissions are attached. |
| <code><a href="#cdk-constructs.ThronNewRelicDockerLambda.property.resourceArnsForGrantInvoke">ResourceArnsForGrantInvoke</a></code> | <code>*[]*string</code> | The ARN(s) to put into the resource field of the generated IAM policy for grantInvoke(). |
| <code><a href="#cdk-constructs.ThronNewRelicDockerLambda.property.role">Role</a></code> | <code>github.com/aws/aws-cdk-go/awscdk/v2.aws_iam.IRole</code> | Execution role associated with this function. |
| <code><a href="#cdk-constructs.ThronNewRelicDockerLambda.property.currentVersion">CurrentVersion</a></code> | <code>github.com/aws/aws-cdk-go/awscdk/v2.aws_lambda.Version</code> | Returns a `lambda.Version` which represents the current version of this Lambda function. A new version will be created every time the function's configuration changes. |
| <code><a href="#cdk-constructs.ThronNewRelicDockerLambda.property.logGroup">LogGroup</a></code> | <code>github.com/aws/aws-cdk-go/awscdk/v2.aws_logs.ILogGroup</code> | The LogGroup where the Lambda function's logs are made available. |
| <code><a href="#cdk-constructs.ThronNewRelicDockerLambda.property.runtime">Runtime</a></code> | <code>github.com/aws/aws-cdk-go/awscdk/v2.aws_lambda.Runtime</code> | The runtime configured for this lambda. |
| <code><a href="#cdk-constructs.ThronNewRelicDockerLambda.property.deadLetterQueue">DeadLetterQueue</a></code> | <code>github.com/aws/aws-cdk-go/awscdk/v2.aws_sqs.IQueue</code> | The DLQ (as queue) associated with this Lambda Function (this is an optional attribute). |
| <code><a href="#cdk-constructs.ThronNewRelicDockerLambda.property.deadLetterTopic">DeadLetterTopic</a></code> | <code>github.com/aws/aws-cdk-go/awscdk/v2.aws_sns.ITopic</code> | The DLQ (as topic) associated with this Lambda Function (this is an optional attribute). |
| <code><a href="#cdk-constructs.ThronNewRelicDockerLambda.property.timeout">Timeout</a></code> | <code>github.com/aws/aws-cdk-go/awscdk/v2.Duration</code> | The timeout configured for this lambda. |
| <code><a href="#cdk-constructs.ThronNewRelicDockerLambda.property.apiGatewayEndpoints">ApiGatewayEndpoints</a></code> | <code>*map[string]<a href="#cdk-constructs.ThronCreatedApiGatewayEndpoint">ThronCreatedApiGatewayEndpoint</a></code> | *No description.* |
| <code><a href="#cdk-constructs.ThronNewRelicDockerLambda.property.endpoints">Endpoints</a></code> | <code>*map[string]<a href="#cdk-constructs.EndpointAlb">EndpointAlb</a></code> | *No description.* |
| <code><a href="#cdk-constructs.ThronNewRelicDockerLambda.property.legacyEndpoints">LegacyEndpoints</a></code> | <code>*map[string]<a href="#cdk-constructs.EndpointAlb">EndpointAlb</a></code> | *No description.* |

---

##### `Node`<sup>Required</sup> <a name="Node" id="cdk-constructs.ThronNewRelicDockerLambda.property.node"></a>

```go
func Node() Node
```

- *Type:* github.com/aws/constructs-go/constructs/v10.Node

The tree node.

---

##### `Env`<sup>Required</sup> <a name="Env" id="cdk-constructs.ThronNewRelicDockerLambda.property.env"></a>

```go
func Env() ResourceEnvironment
```

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.ResourceEnvironment

The environment this resource belongs to.

For resources that are created and managed by the CDK
(generally, those created by creating new class instances like Role, Bucket, etc.),
this is always the same as the environment of the stack they belong to;
however, for imported resources
(those obtained from static methods like fromRoleArn, fromBucketName, etc.),
that might be different than the stack they were imported into.

---

##### `Stack`<sup>Required</sup> <a name="Stack" id="cdk-constructs.ThronNewRelicDockerLambda.property.stack"></a>

```go
func Stack() Stack
```

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.Stack

The stack in which this resource is defined.

---

##### `Architecture`<sup>Required</sup> <a name="Architecture" id="cdk-constructs.ThronNewRelicDockerLambda.property.architecture"></a>

```go
func Architecture() Architecture
```

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_lambda.Architecture

The architecture of this Lambda Function (this is an optional attribute and defaults to X86_64).

---

##### `Connections`<sup>Required</sup> <a name="Connections" id="cdk-constructs.ThronNewRelicDockerLambda.property.connections"></a>

```go
func Connections() Connections
```

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_ec2.Connections

Access the Connections object.

Will fail if not a VPC-enabled Lambda Function

---

##### `FunctionArn`<sup>Required</sup> <a name="FunctionArn" id="cdk-constructs.ThronNewRelicDockerLambda.property.functionArn"></a>

```go
func FunctionArn() *string
```

- *Type:* *string

ARN of this function.

---

##### `FunctionName`<sup>Required</sup> <a name="FunctionName" id="cdk-constructs.ThronNewRelicDockerLambda.property.functionName"></a>

```go
func FunctionName() *string
```

- *Type:* *string

Name of this function.

---

##### `GrantPrincipal`<sup>Required</sup> <a name="GrantPrincipal" id="cdk-constructs.ThronNewRelicDockerLambda.property.grantPrincipal"></a>

```go
func GrantPrincipal() IPrincipal
```

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_iam.IPrincipal

The principal this Lambda Function is running as.

---

##### `IsBoundToVpc`<sup>Required</sup> <a name="IsBoundToVpc" id="cdk-constructs.ThronNewRelicDockerLambda.property.isBoundToVpc"></a>

```go
func IsBoundToVpc() *bool
```

- *Type:* *bool

Whether or not this Lambda function was bound to a VPC.

If this is is `false`, trying to access the `connections` object will fail.

---

##### `LatestVersion`<sup>Required</sup> <a name="LatestVersion" id="cdk-constructs.ThronNewRelicDockerLambda.property.latestVersion"></a>

```go
func LatestVersion() IVersion
```

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_lambda.IVersion

The `$LATEST` version of this function.

Note that this is reference to a non-specific AWS Lambda version, which
means the function this version refers to can return different results in
different invocations.

To obtain a reference to an explicit version which references the current
function configuration, use `lambdaFunction.currentVersion` instead.

---

##### `PermissionsNode`<sup>Required</sup> <a name="PermissionsNode" id="cdk-constructs.ThronNewRelicDockerLambda.property.permissionsNode"></a>

```go
func PermissionsNode() Node
```

- *Type:* github.com/aws/constructs-go/constructs/v10.Node

The construct node where permissions are attached.

---

##### `ResourceArnsForGrantInvoke`<sup>Required</sup> <a name="ResourceArnsForGrantInvoke" id="cdk-constructs.ThronNewRelicDockerLambda.property.resourceArnsForGrantInvoke"></a>

```go
func ResourceArnsForGrantInvoke() *[]*string
```

- *Type:* *[]*string

The ARN(s) to put into the resource field of the generated IAM policy for grantInvoke().

---

##### `Role`<sup>Optional</sup> <a name="Role" id="cdk-constructs.ThronNewRelicDockerLambda.property.role"></a>

```go
func Role() IRole
```

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_iam.IRole

Execution role associated with this function.

---

##### `CurrentVersion`<sup>Required</sup> <a name="CurrentVersion" id="cdk-constructs.ThronNewRelicDockerLambda.property.currentVersion"></a>

```go
func CurrentVersion() Version
```

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_lambda.Version

Returns a `lambda.Version` which represents the current version of this Lambda function. A new version will be created every time the function's configuration changes.

You can specify options for this version using the `currentVersionOptions`
prop when initializing the `lambda.Function`.

---

##### `LogGroup`<sup>Required</sup> <a name="LogGroup" id="cdk-constructs.ThronNewRelicDockerLambda.property.logGroup"></a>

```go
func LogGroup() ILogGroup
```

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_logs.ILogGroup

The LogGroup where the Lambda function's logs are made available.

If either `logRetention` is set or this property is called, a CloudFormation custom resource is added to the stack that
pre-creates the log group as part of the stack deployment, if it already doesn't exist, and sets the correct log retention
period (never expire, by default).

Further, if the log group already exists and the `logRetention` is not set, the custom resource will reset the log retention
to never expire even if it was configured with a different value.

---

##### `Runtime`<sup>Required</sup> <a name="Runtime" id="cdk-constructs.ThronNewRelicDockerLambda.property.runtime"></a>

```go
func Runtime() Runtime
```

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_lambda.Runtime

The runtime configured for this lambda.

---

##### `DeadLetterQueue`<sup>Optional</sup> <a name="DeadLetterQueue" id="cdk-constructs.ThronNewRelicDockerLambda.property.deadLetterQueue"></a>

```go
func DeadLetterQueue() IQueue
```

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_sqs.IQueue

The DLQ (as queue) associated with this Lambda Function (this is an optional attribute).

---

##### `DeadLetterTopic`<sup>Optional</sup> <a name="DeadLetterTopic" id="cdk-constructs.ThronNewRelicDockerLambda.property.deadLetterTopic"></a>

```go
func DeadLetterTopic() ITopic
```

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_sns.ITopic

The DLQ (as topic) associated with this Lambda Function (this is an optional attribute).

---

##### `Timeout`<sup>Optional</sup> <a name="Timeout" id="cdk-constructs.ThronNewRelicDockerLambda.property.timeout"></a>

```go
func Timeout() Duration
```

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.Duration

The timeout configured for this lambda.

---

##### `ApiGatewayEndpoints`<sup>Optional</sup> <a name="ApiGatewayEndpoints" id="cdk-constructs.ThronNewRelicDockerLambda.property.apiGatewayEndpoints"></a>

```go
func ApiGatewayEndpoints() *map[string]ThronCreatedApiGatewayEndpoint
```

- *Type:* *map[string]<a href="#cdk-constructs.ThronCreatedApiGatewayEndpoint">ThronCreatedApiGatewayEndpoint</a>

---

##### `Endpoints`<sup>Optional</sup> <a name="Endpoints" id="cdk-constructs.ThronNewRelicDockerLambda.property.endpoints"></a>

```go
func Endpoints() *map[string]EndpointAlb
```

- *Type:* *map[string]<a href="#cdk-constructs.EndpointAlb">EndpointAlb</a>

---

##### `LegacyEndpoints`<sup>Optional</sup> <a name="LegacyEndpoints" id="cdk-constructs.ThronNewRelicDockerLambda.property.legacyEndpoints"></a>

```go
func LegacyEndpoints() *map[string]EndpointAlb
```

- *Type:* *map[string]<a href="#cdk-constructs.EndpointAlb">EndpointAlb</a>

---


### ThronPipelineBuildProject <a name="ThronPipelineBuildProject" id="cdk-constructs.ThronPipelineBuildProject"></a>

- *Implements:* github.com/aws/aws-cdk-go/awscdk/v2.aws_iam.IGrantable

#### Initializers <a name="Initializers" id="cdk-constructs.ThronPipelineBuildProject.Initializer"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

cdkconstructs.NewThronPipelineBuildProject(scope Construct, id *string, props ThronPipelineBuildProjectProps) ThronPipelineBuildProject
```

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.ThronPipelineBuildProject.Initializer.parameter.scope">scope</a></code> | <code>github.com/aws/constructs-go/constructs/v10.Construct</code> | *No description.* |
| <code><a href="#cdk-constructs.ThronPipelineBuildProject.Initializer.parameter.id">id</a></code> | <code>*string</code> | *No description.* |
| <code><a href="#cdk-constructs.ThronPipelineBuildProject.Initializer.parameter.props">props</a></code> | <code><a href="#cdk-constructs.ThronPipelineBuildProjectProps">ThronPipelineBuildProjectProps</a></code> | *No description.* |

---

##### `scope`<sup>Required</sup> <a name="scope" id="cdk-constructs.ThronPipelineBuildProject.Initializer.parameter.scope"></a>

- *Type:* github.com/aws/constructs-go/constructs/v10.Construct

---

##### `id`<sup>Required</sup> <a name="id" id="cdk-constructs.ThronPipelineBuildProject.Initializer.parameter.id"></a>

- *Type:* *string

---

##### `props`<sup>Required</sup> <a name="props" id="cdk-constructs.ThronPipelineBuildProject.Initializer.parameter.props"></a>

- *Type:* <a href="#cdk-constructs.ThronPipelineBuildProjectProps">ThronPipelineBuildProjectProps</a>

---

#### Methods <a name="Methods" id="Methods"></a>

| **Name** | **Description** |
| --- | --- |
| <code><a href="#cdk-constructs.ThronPipelineBuildProject.toString">ToString</a></code> | Returns a string representation of this construct. |
| <code><a href="#cdk-constructs.ThronPipelineBuildProject.allowCDKAccessToAccount">AllowCDKAccessToAccount</a></code> | *No description.* |
| <code><a href="#cdk-constructs.ThronPipelineBuildProject.allowEcrForRepo">AllowEcrForRepo</a></code> | *No description.* |

---

##### `ToString` <a name="ToString" id="cdk-constructs.ThronPipelineBuildProject.toString"></a>

```go
func ToString() *string
```

Returns a string representation of this construct.

##### `AllowCDKAccessToAccount` <a name="AllowCDKAccessToAccount" id="cdk-constructs.ThronPipelineBuildProject.allowCDKAccessToAccount"></a>

```go
func AllowCDKAccessToAccount(accountId *string)
```

###### `accountId`<sup>Required</sup> <a name="accountId" id="cdk-constructs.ThronPipelineBuildProject.allowCDKAccessToAccount.parameter.accountId"></a>

- *Type:* *string

---

##### `AllowEcrForRepo` <a name="AllowEcrForRepo" id="cdk-constructs.ThronPipelineBuildProject.allowEcrForRepo"></a>

```go
func AllowEcrForRepo(ecrRepository Repository)
```

###### `ecrRepository`<sup>Required</sup> <a name="ecrRepository" id="cdk-constructs.ThronPipelineBuildProject.allowEcrForRepo.parameter.ecrRepository"></a>

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_ecr.Repository

---

#### Static Functions <a name="Static Functions" id="Static Functions"></a>

| **Name** | **Description** |
| --- | --- |
| <code><a href="#cdk-constructs.ThronPipelineBuildProject.isConstruct">IsConstruct</a></code> | Checks if `x` is a construct. |

---

##### `IsConstruct` <a name="IsConstruct" id="cdk-constructs.ThronPipelineBuildProject.isConstruct"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

cdkconstructs.ThronPipelineBuildProject_IsConstruct(x interface{}) *bool
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

- *Type:* interface{}

Any object.

---

#### Properties <a name="Properties" id="Properties"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.ThronPipelineBuildProject.property.node">Node</a></code> | <code>github.com/aws/constructs-go/constructs/v10.Node</code> | The tree node. |
| <code><a href="#cdk-constructs.ThronPipelineBuildProject.property.grantPrincipal">GrantPrincipal</a></code> | <code>github.com/aws/aws-cdk-go/awscdk/v2.aws_iam.IPrincipal</code> | The principal to grant permissions to. |
| <code><a href="#cdk-constructs.ThronPipelineBuildProject.property.buildName">BuildName</a></code> | <code>*string</code> | *No description.* |
| <code><a href="#cdk-constructs.ThronPipelineBuildProject.property.project">Project</a></code> | <code>github.com/aws/aws-cdk-go/awscdk/v2.aws_codebuild.Project</code> | *No description.* |
| <code><a href="#cdk-constructs.ThronPipelineBuildProject.property.role">Role</a></code> | <code>github.com/aws/aws-cdk-go/awscdk/v2.aws_iam.Role</code> | *No description.* |

---

##### `Node`<sup>Required</sup> <a name="Node" id="cdk-constructs.ThronPipelineBuildProject.property.node"></a>

```go
func Node() Node
```

- *Type:* github.com/aws/constructs-go/constructs/v10.Node

The tree node.

---

##### `GrantPrincipal`<sup>Required</sup> <a name="GrantPrincipal" id="cdk-constructs.ThronPipelineBuildProject.property.grantPrincipal"></a>

```go
func GrantPrincipal() IPrincipal
```

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_iam.IPrincipal

The principal to grant permissions to.

---

##### `BuildName`<sup>Required</sup> <a name="BuildName" id="cdk-constructs.ThronPipelineBuildProject.property.buildName"></a>

```go
func BuildName() *string
```

- *Type:* *string

---

##### `Project`<sup>Required</sup> <a name="Project" id="cdk-constructs.ThronPipelineBuildProject.property.project"></a>

```go
func Project() Project
```

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_codebuild.Project

---

##### `Role`<sup>Required</sup> <a name="Role" id="cdk-constructs.ThronPipelineBuildProject.property.role"></a>

```go
func Role() Role
```

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_iam.Role

---


### ThronResponseHeaderPolicy <a name="ThronResponseHeaderPolicy" id="cdk-constructs.ThronResponseHeaderPolicy"></a>

#### Initializers <a name="Initializers" id="cdk-constructs.ThronResponseHeaderPolicy.Initializer"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

cdkconstructs.NewThronResponseHeaderPolicy(scope Construct, id *string, props ResponseHeadersPolicyProps) ThronResponseHeaderPolicy
```

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.ThronResponseHeaderPolicy.Initializer.parameter.scope">scope</a></code> | <code>github.com/aws/constructs-go/constructs/v10.Construct</code> | *No description.* |
| <code><a href="#cdk-constructs.ThronResponseHeaderPolicy.Initializer.parameter.id">id</a></code> | <code>*string</code> | *No description.* |
| <code><a href="#cdk-constructs.ThronResponseHeaderPolicy.Initializer.parameter.props">props</a></code> | <code>github.com/aws/aws-cdk-go/awscdk/v2.aws_cloudfront.ResponseHeadersPolicyProps</code> | *No description.* |

---

##### `scope`<sup>Required</sup> <a name="scope" id="cdk-constructs.ThronResponseHeaderPolicy.Initializer.parameter.scope"></a>

- *Type:* github.com/aws/constructs-go/constructs/v10.Construct

---

##### `id`<sup>Required</sup> <a name="id" id="cdk-constructs.ThronResponseHeaderPolicy.Initializer.parameter.id"></a>

- *Type:* *string

---

##### `props`<sup>Optional</sup> <a name="props" id="cdk-constructs.ThronResponseHeaderPolicy.Initializer.parameter.props"></a>

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_cloudfront.ResponseHeadersPolicyProps

---

#### Methods <a name="Methods" id="Methods"></a>

| **Name** | **Description** |
| --- | --- |
| <code><a href="#cdk-constructs.ThronResponseHeaderPolicy.toString">ToString</a></code> | Returns a string representation of this construct. |
| <code><a href="#cdk-constructs.ThronResponseHeaderPolicy.applyRemovalPolicy">ApplyRemovalPolicy</a></code> | Apply the given removal policy to this resource. |

---

##### `ToString` <a name="ToString" id="cdk-constructs.ThronResponseHeaderPolicy.toString"></a>

```go
func ToString() *string
```

Returns a string representation of this construct.

##### `ApplyRemovalPolicy` <a name="ApplyRemovalPolicy" id="cdk-constructs.ThronResponseHeaderPolicy.applyRemovalPolicy"></a>

```go
func ApplyRemovalPolicy(policy RemovalPolicy)
```

Apply the given removal policy to this resource.

The Removal Policy controls what happens to this resource when it stops
being managed by CloudFormation, either because you've removed it from the
CDK application or because you've made a change that requires the resource
to be replaced.

The resource can be deleted (`RemovalPolicy.DESTROY`), or left in your AWS
account for data recovery and cleanup later (`RemovalPolicy.RETAIN`).

###### `policy`<sup>Required</sup> <a name="policy" id="cdk-constructs.ThronResponseHeaderPolicy.applyRemovalPolicy.parameter.policy"></a>

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.RemovalPolicy

---

#### Static Functions <a name="Static Functions" id="Static Functions"></a>

| **Name** | **Description** |
| --- | --- |
| <code><a href="#cdk-constructs.ThronResponseHeaderPolicy.isConstruct">IsConstruct</a></code> | Checks if `x` is a construct. |
| <code><a href="#cdk-constructs.ThronResponseHeaderPolicy.isOwnedResource">IsOwnedResource</a></code> | Returns true if the construct was created by CDK, and false otherwise. |
| <code><a href="#cdk-constructs.ThronResponseHeaderPolicy.isResource">IsResource</a></code> | Check whether the given construct is a Resource. |
| <code><a href="#cdk-constructs.ThronResponseHeaderPolicy.fromResponseHeadersPolicyId">FromResponseHeadersPolicyId</a></code> | Import an existing Response Headers Policy from its ID. |
| <code><a href="#cdk-constructs.ThronResponseHeaderPolicy.default">Default</a></code> | Generates a `ThronResponseHeaderPolicy` with all the default values. |
| <code><a href="#cdk-constructs.ThronResponseHeaderPolicy.defaultWithOverrides">DefaultWithOverrides</a></code> | Generates a `ThronResponseHeaderPolicy` with all the default values except for the ones passed on `props`. |

---

##### `IsConstruct` <a name="IsConstruct" id="cdk-constructs.ThronResponseHeaderPolicy.isConstruct"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

cdkconstructs.ThronResponseHeaderPolicy_IsConstruct(x interface{}) *bool
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

- *Type:* interface{}

Any object.

---

##### `IsOwnedResource` <a name="IsOwnedResource" id="cdk-constructs.ThronResponseHeaderPolicy.isOwnedResource"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

cdkconstructs.ThronResponseHeaderPolicy_IsOwnedResource(construct IConstruct) *bool
```

Returns true if the construct was created by CDK, and false otherwise.

###### `construct`<sup>Required</sup> <a name="construct" id="cdk-constructs.ThronResponseHeaderPolicy.isOwnedResource.parameter.construct"></a>

- *Type:* github.com/aws/constructs-go/constructs/v10.IConstruct

---

##### `IsResource` <a name="IsResource" id="cdk-constructs.ThronResponseHeaderPolicy.isResource"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

cdkconstructs.ThronResponseHeaderPolicy_IsResource(construct IConstruct) *bool
```

Check whether the given construct is a Resource.

###### `construct`<sup>Required</sup> <a name="construct" id="cdk-constructs.ThronResponseHeaderPolicy.isResource.parameter.construct"></a>

- *Type:* github.com/aws/constructs-go/constructs/v10.IConstruct

---

##### `FromResponseHeadersPolicyId` <a name="FromResponseHeadersPolicyId" id="cdk-constructs.ThronResponseHeaderPolicy.fromResponseHeadersPolicyId"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

cdkconstructs.ThronResponseHeaderPolicy_FromResponseHeadersPolicyId(scope Construct, id *string, responseHeadersPolicyId *string) IResponseHeadersPolicy
```

Import an existing Response Headers Policy from its ID.

###### `scope`<sup>Required</sup> <a name="scope" id="cdk-constructs.ThronResponseHeaderPolicy.fromResponseHeadersPolicyId.parameter.scope"></a>

- *Type:* github.com/aws/constructs-go/constructs/v10.Construct

---

###### `id`<sup>Required</sup> <a name="id" id="cdk-constructs.ThronResponseHeaderPolicy.fromResponseHeadersPolicyId.parameter.id"></a>

- *Type:* *string

---

###### `responseHeadersPolicyId`<sup>Required</sup> <a name="responseHeadersPolicyId" id="cdk-constructs.ThronResponseHeaderPolicy.fromResponseHeadersPolicyId.parameter.responseHeadersPolicyId"></a>

- *Type:* *string

---

##### `Default` <a name="Default" id="cdk-constructs.ThronResponseHeaderPolicy.default"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

cdkconstructs.ThronResponseHeaderPolicy_Default(scope Construct, id *string) ThronResponseHeaderPolicy
```

Generates a `ThronResponseHeaderPolicy` with all the default values.

###### `scope`<sup>Required</sup> <a name="scope" id="cdk-constructs.ThronResponseHeaderPolicy.default.parameter.scope"></a>

- *Type:* github.com/aws/constructs-go/constructs/v10.Construct

---

###### `id`<sup>Required</sup> <a name="id" id="cdk-constructs.ThronResponseHeaderPolicy.default.parameter.id"></a>

- *Type:* *string

---

##### `DefaultWithOverrides` <a name="DefaultWithOverrides" id="cdk-constructs.ThronResponseHeaderPolicy.defaultWithOverrides"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

cdkconstructs.ThronResponseHeaderPolicy_DefaultWithOverrides(scope Construct, id *string, props ThronResponseHeaderPolicyProps) ThronResponseHeaderPolicy
```

Generates a `ThronResponseHeaderPolicy` with all the default values except for the ones passed on `props`.

###### `scope`<sup>Required</sup> <a name="scope" id="cdk-constructs.ThronResponseHeaderPolicy.defaultWithOverrides.parameter.scope"></a>

- *Type:* github.com/aws/constructs-go/constructs/v10.Construct

---

###### `id`<sup>Required</sup> <a name="id" id="cdk-constructs.ThronResponseHeaderPolicy.defaultWithOverrides.parameter.id"></a>

- *Type:* *string

---

###### `props`<sup>Required</sup> <a name="props" id="cdk-constructs.ThronResponseHeaderPolicy.defaultWithOverrides.parameter.props"></a>

- *Type:* <a href="#cdk-constructs.ThronResponseHeaderPolicyProps">ThronResponseHeaderPolicyProps</a>

---

#### Properties <a name="Properties" id="Properties"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.ThronResponseHeaderPolicy.property.node">Node</a></code> | <code>github.com/aws/constructs-go/constructs/v10.Node</code> | The tree node. |
| <code><a href="#cdk-constructs.ThronResponseHeaderPolicy.property.env">Env</a></code> | <code>github.com/aws/aws-cdk-go/awscdk/v2.ResourceEnvironment</code> | The environment this resource belongs to. |
| <code><a href="#cdk-constructs.ThronResponseHeaderPolicy.property.stack">Stack</a></code> | <code>github.com/aws/aws-cdk-go/awscdk/v2.Stack</code> | The stack in which this resource is defined. |
| <code><a href="#cdk-constructs.ThronResponseHeaderPolicy.property.responseHeadersPolicyId">ResponseHeadersPolicyId</a></code> | <code>*string</code> | The ID of the response headers policy. |

---

##### `Node`<sup>Required</sup> <a name="Node" id="cdk-constructs.ThronResponseHeaderPolicy.property.node"></a>

```go
func Node() Node
```

- *Type:* github.com/aws/constructs-go/constructs/v10.Node

The tree node.

---

##### `Env`<sup>Required</sup> <a name="Env" id="cdk-constructs.ThronResponseHeaderPolicy.property.env"></a>

```go
func Env() ResourceEnvironment
```

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.ResourceEnvironment

The environment this resource belongs to.

For resources that are created and managed by the CDK
(generally, those created by creating new class instances like Role, Bucket, etc.),
this is always the same as the environment of the stack they belong to;
however, for imported resources
(those obtained from static methods like fromRoleArn, fromBucketName, etc.),
that might be different than the stack they were imported into.

---

##### `Stack`<sup>Required</sup> <a name="Stack" id="cdk-constructs.ThronResponseHeaderPolicy.property.stack"></a>

```go
func Stack() Stack
```

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.Stack

The stack in which this resource is defined.

---

##### `ResponseHeadersPolicyId`<sup>Required</sup> <a name="ResponseHeadersPolicyId" id="cdk-constructs.ThronResponseHeaderPolicy.property.responseHeadersPolicyId"></a>

```go
func ResponseHeadersPolicyId() *string
```

- *Type:* *string

The ID of the response headers policy.

---

#### Constants <a name="Constants" id="Constants"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.ThronResponseHeaderPolicy.property.CORS_ALLOW_ALL_ORIGINS">CorsAllowAllOrigins</a></code> | <code>github.com/aws/aws-cdk-go/awscdk/v2.aws_cloudfront.IResponseHeadersPolicy</code> | Use this managed policy to allow simple CORS requests from any origin. |
| <code><a href="#cdk-constructs.ThronResponseHeaderPolicy.property.CORS_ALLOW_ALL_ORIGINS_AND_SECURITY_HEADERS">CorsAllowAllOriginsAndSecurityHeaders</a></code> | <code>github.com/aws/aws-cdk-go/awscdk/v2.aws_cloudfront.IResponseHeadersPolicy</code> | Use this managed policy to allow simple CORS requests from any origin and add a set of security headers to all responses that CloudFront sends to viewers. |
| <code><a href="#cdk-constructs.ThronResponseHeaderPolicy.property.CORS_ALLOW_ALL_ORIGINS_WITH_PREFLIGHT">CorsAllowAllOriginsWithPreflight</a></code> | <code>github.com/aws/aws-cdk-go/awscdk/v2.aws_cloudfront.IResponseHeadersPolicy</code> | Use this managed policy to allow CORS requests from any origin, including preflight requests. |
| <code><a href="#cdk-constructs.ThronResponseHeaderPolicy.property.CORS_ALLOW_ALL_ORIGINS_WITH_PREFLIGHT_AND_SECURITY_HEADERS">CorsAllowAllOriginsWithPreflightAndSecurityHeaders</a></code> | <code>github.com/aws/aws-cdk-go/awscdk/v2.aws_cloudfront.IResponseHeadersPolicy</code> | Use this managed policy to allow CORS requests from any origin, including preflight requests, and add a set of security headers to all responses that CloudFront sends to viewers. |
| <code><a href="#cdk-constructs.ThronResponseHeaderPolicy.property.SECURITY_HEADERS">SecurityHeaders</a></code> | <code>github.com/aws/aws-cdk-go/awscdk/v2.aws_cloudfront.IResponseHeadersPolicy</code> | Use this managed policy to add a set of security headers to all responses that CloudFront sends to viewers. |

---

##### `CorsAllowAllOrigins`<sup>Required</sup> <a name="CorsAllowAllOrigins" id="cdk-constructs.ThronResponseHeaderPolicy.property.CORS_ALLOW_ALL_ORIGINS"></a>

```go
func CorsAllowAllOrigins() IResponseHeadersPolicy
```

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_cloudfront.IResponseHeadersPolicy

Use this managed policy to allow simple CORS requests from any origin.

---

##### `CorsAllowAllOriginsAndSecurityHeaders`<sup>Required</sup> <a name="CorsAllowAllOriginsAndSecurityHeaders" id="cdk-constructs.ThronResponseHeaderPolicy.property.CORS_ALLOW_ALL_ORIGINS_AND_SECURITY_HEADERS"></a>

```go
func CorsAllowAllOriginsAndSecurityHeaders() IResponseHeadersPolicy
```

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_cloudfront.IResponseHeadersPolicy

Use this managed policy to allow simple CORS requests from any origin and add a set of security headers to all responses that CloudFront sends to viewers.

---

##### `CorsAllowAllOriginsWithPreflight`<sup>Required</sup> <a name="CorsAllowAllOriginsWithPreflight" id="cdk-constructs.ThronResponseHeaderPolicy.property.CORS_ALLOW_ALL_ORIGINS_WITH_PREFLIGHT"></a>

```go
func CorsAllowAllOriginsWithPreflight() IResponseHeadersPolicy
```

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_cloudfront.IResponseHeadersPolicy

Use this managed policy to allow CORS requests from any origin, including preflight requests.

---

##### `CorsAllowAllOriginsWithPreflightAndSecurityHeaders`<sup>Required</sup> <a name="CorsAllowAllOriginsWithPreflightAndSecurityHeaders" id="cdk-constructs.ThronResponseHeaderPolicy.property.CORS_ALLOW_ALL_ORIGINS_WITH_PREFLIGHT_AND_SECURITY_HEADERS"></a>

```go
func CorsAllowAllOriginsWithPreflightAndSecurityHeaders() IResponseHeadersPolicy
```

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_cloudfront.IResponseHeadersPolicy

Use this managed policy to allow CORS requests from any origin, including preflight requests, and add a set of security headers to all responses that CloudFront sends to viewers.

---

##### `SecurityHeaders`<sup>Required</sup> <a name="SecurityHeaders" id="cdk-constructs.ThronResponseHeaderPolicy.property.SECURITY_HEADERS"></a>

```go
func SecurityHeaders() IResponseHeadersPolicy
```

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_cloudfront.IResponseHeadersPolicy

Use this managed policy to add a set of security headers to all responses that CloudFront sends to viewers.

---

### ThronStack <a name="ThronStack" id="cdk-constructs.ThronStack"></a>

#### Initializers <a name="Initializers" id="cdk-constructs.ThronStack.Initializer"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

cdkconstructs.NewThronStack(scope App, description *string, suffix *string, overrideAccount *string, overrideRegion *string) ThronStack
```

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.ThronStack.Initializer.parameter.scope">scope</a></code> | <code>github.com/aws/aws-cdk-go/awscdk/v2.App</code> | *No description.* |
| <code><a href="#cdk-constructs.ThronStack.Initializer.parameter.description">description</a></code> | <code>*string</code> | *No description.* |
| <code><a href="#cdk-constructs.ThronStack.Initializer.parameter.suffix">suffix</a></code> | <code>*string</code> | *No description.* |
| <code><a href="#cdk-constructs.ThronStack.Initializer.parameter.overrideAccount">overrideAccount</a></code> | <code>*string</code> | *No description.* |
| <code><a href="#cdk-constructs.ThronStack.Initializer.parameter.overrideRegion">overrideRegion</a></code> | <code>*string</code> | *No description.* |

---

##### `scope`<sup>Required</sup> <a name="scope" id="cdk-constructs.ThronStack.Initializer.parameter.scope"></a>

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.App

---

##### `description`<sup>Optional</sup> <a name="description" id="cdk-constructs.ThronStack.Initializer.parameter.description"></a>

- *Type:* *string

---

##### `suffix`<sup>Optional</sup> <a name="suffix" id="cdk-constructs.ThronStack.Initializer.parameter.suffix"></a>

- *Type:* *string

---

##### `overrideAccount`<sup>Optional</sup> <a name="overrideAccount" id="cdk-constructs.ThronStack.Initializer.parameter.overrideAccount"></a>

- *Type:* *string

---

##### `overrideRegion`<sup>Optional</sup> <a name="overrideRegion" id="cdk-constructs.ThronStack.Initializer.parameter.overrideRegion"></a>

- *Type:* *string

---

#### Methods <a name="Methods" id="Methods"></a>

| **Name** | **Description** |
| --- | --- |
| <code><a href="#cdk-constructs.ThronStack.toString">ToString</a></code> | Returns a string representation of this construct. |
| <code><a href="#cdk-constructs.ThronStack.addDependency">AddDependency</a></code> | Add a dependency between this stack and another stack. |
| <code><a href="#cdk-constructs.ThronStack.addMetadata">AddMetadata</a></code> | Adds an arbitrary key-value pair, with information you want to record about the stack. |
| <code><a href="#cdk-constructs.ThronStack.addTransform">AddTransform</a></code> | Add a Transform to this stack. A Transform is a macro that AWS CloudFormation uses to process your template. |
| <code><a href="#cdk-constructs.ThronStack.exportStringListValue">ExportStringListValue</a></code> | Create a CloudFormation Export for a string list value. |
| <code><a href="#cdk-constructs.ThronStack.exportValue">ExportValue</a></code> | Create a CloudFormation Export for a string value. |
| <code><a href="#cdk-constructs.ThronStack.formatArn">FormatArn</a></code> | Creates an ARN from components. |
| <code><a href="#cdk-constructs.ThronStack.getLogicalId">GetLogicalId</a></code> | Allocates a stack-unique CloudFormation-compatible logical identity for a specific resource. |
| <code><a href="#cdk-constructs.ThronStack.regionalFact">RegionalFact</a></code> | Look up a fact value for the given fact for the region of this stack. |
| <code><a href="#cdk-constructs.ThronStack.renameLogicalId">RenameLogicalId</a></code> | Rename a generated logical identities. |
| <code><a href="#cdk-constructs.ThronStack.reportMissingContextKey">ReportMissingContextKey</a></code> | Indicate that a context key was expected. |
| <code><a href="#cdk-constructs.ThronStack.resolve">Resolve</a></code> | Resolve a tokenized value in the context of the current stack. |
| <code><a href="#cdk-constructs.ThronStack.splitArn">SplitArn</a></code> | Splits the provided ARN into its components. |
| <code><a href="#cdk-constructs.ThronStack.toJsonString">ToJsonString</a></code> | Convert an object, potentially containing tokens, to a JSON string. |
| <code><a href="#cdk-constructs.ThronStack.toYamlString">ToYamlString</a></code> | Convert an object, potentially containing tokens, to a YAML string. |

---

##### `ToString` <a name="ToString" id="cdk-constructs.ThronStack.toString"></a>

```go
func ToString() *string
```

Returns a string representation of this construct.

##### `AddDependency` <a name="AddDependency" id="cdk-constructs.ThronStack.addDependency"></a>

```go
func AddDependency(target Stack, reason *string)
```

Add a dependency between this stack and another stack.

This can be used to define dependencies between any two stacks within an
app, and also supports nested stacks.

###### `target`<sup>Required</sup> <a name="target" id="cdk-constructs.ThronStack.addDependency.parameter.target"></a>

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.Stack

---

###### `reason`<sup>Optional</sup> <a name="reason" id="cdk-constructs.ThronStack.addDependency.parameter.reason"></a>

- *Type:* *string

---

##### `AddMetadata` <a name="AddMetadata" id="cdk-constructs.ThronStack.addMetadata"></a>

```go
func AddMetadata(key *string, value interface{})
```

Adds an arbitrary key-value pair, with information you want to record about the stack.

These get translated to the Metadata section of the generated template.

> [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/metadata-section-structure.html](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/metadata-section-structure.html)

###### `key`<sup>Required</sup> <a name="key" id="cdk-constructs.ThronStack.addMetadata.parameter.key"></a>

- *Type:* *string

---

###### `value`<sup>Required</sup> <a name="value" id="cdk-constructs.ThronStack.addMetadata.parameter.value"></a>

- *Type:* interface{}

---

##### `AddTransform` <a name="AddTransform" id="cdk-constructs.ThronStack.addTransform"></a>

```go
func AddTransform(transform *string)
```

Add a Transform to this stack. A Transform is a macro that AWS CloudFormation uses to process your template.

Duplicate values are removed when stack is synthesized.

> [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/transform-section-structure.html](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/transform-section-structure.html)

*Example*

```go
declare const stack: Stack;

stack.addTransform('AWS::Serverless-2016-10-31')
```


###### `transform`<sup>Required</sup> <a name="transform" id="cdk-constructs.ThronStack.addTransform.parameter.transform"></a>

- *Type:* *string

The transform to add.

---

##### `ExportStringListValue` <a name="ExportStringListValue" id="cdk-constructs.ThronStack.exportStringListValue"></a>

```go
func ExportStringListValue(exportedValue interface{}, options ExportValueOptions) *[]*string
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

- *Type:* interface{}

---

###### `options`<sup>Optional</sup> <a name="options" id="cdk-constructs.ThronStack.exportStringListValue.parameter.options"></a>

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.ExportValueOptions

---

##### `ExportValue` <a name="ExportValue" id="cdk-constructs.ThronStack.exportValue"></a>

```go
func ExportValue(exportedValue interface{}, options ExportValueOptions) *string
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

- *Type:* interface{}

---

###### `options`<sup>Optional</sup> <a name="options" id="cdk-constructs.ThronStack.exportValue.parameter.options"></a>

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.ExportValueOptions

---

##### `FormatArn` <a name="FormatArn" id="cdk-constructs.ThronStack.formatArn"></a>

```go
func FormatArn(components ArnComponents) *string
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

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.ArnComponents

---

##### `GetLogicalId` <a name="GetLogicalId" id="cdk-constructs.ThronStack.getLogicalId"></a>

```go
func GetLogicalId(element CfnElement) *string
```

Allocates a stack-unique CloudFormation-compatible logical identity for a specific resource.

This method is called when a `CfnElement` is created and used to render the
initial logical identity of resources. Logical ID renames are applied at
this stage.

This method uses the protected method `allocateLogicalId` to render the
logical ID for an element. To modify the naming scheme, extend the `Stack`
class and override this method.

###### `element`<sup>Required</sup> <a name="element" id="cdk-constructs.ThronStack.getLogicalId.parameter.element"></a>

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.CfnElement

The CloudFormation element for which a logical identity is needed.

---

##### `RegionalFact` <a name="RegionalFact" id="cdk-constructs.ThronStack.regionalFact"></a>

```go
func RegionalFact(factName *string, defaultValue *string) *string
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

- *Type:* *string

---

###### `defaultValue`<sup>Optional</sup> <a name="defaultValue" id="cdk-constructs.ThronStack.regionalFact.parameter.defaultValue"></a>

- *Type:* *string

---

##### `RenameLogicalId` <a name="RenameLogicalId" id="cdk-constructs.ThronStack.renameLogicalId"></a>

```go
func RenameLogicalId(oldId *string, newId *string)
```

Rename a generated logical identities.

To modify the naming scheme strategy, extend the `Stack` class and
override the `allocateLogicalId` method.

###### `oldId`<sup>Required</sup> <a name="oldId" id="cdk-constructs.ThronStack.renameLogicalId.parameter.oldId"></a>

- *Type:* *string

---

###### `newId`<sup>Required</sup> <a name="newId" id="cdk-constructs.ThronStack.renameLogicalId.parameter.newId"></a>

- *Type:* *string

---

##### `ReportMissingContextKey` <a name="ReportMissingContextKey" id="cdk-constructs.ThronStack.reportMissingContextKey"></a>

```go
func ReportMissingContextKey(report MissingContext)
```

Indicate that a context key was expected.

Contains instructions which will be emitted into the cloud assembly on how
the key should be supplied.

###### `report`<sup>Required</sup> <a name="report" id="cdk-constructs.ThronStack.reportMissingContextKey.parameter.report"></a>

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.cloud_assembly_schema.MissingContext

The set of parameters needed to obtain the context.

---

##### `Resolve` <a name="Resolve" id="cdk-constructs.ThronStack.resolve"></a>

```go
func Resolve(obj interface{}) interface{}
```

Resolve a tokenized value in the context of the current stack.

###### `obj`<sup>Required</sup> <a name="obj" id="cdk-constructs.ThronStack.resolve.parameter.obj"></a>

- *Type:* interface{}

---

##### `SplitArn` <a name="SplitArn" id="cdk-constructs.ThronStack.splitArn"></a>

```go
func SplitArn(arn *string, arnFormat ArnFormat) ArnComponents
```

Splits the provided ARN into its components.

Works both if 'arn' is a string like 'arn:aws:s3:::bucket',
and a Token representing a dynamic CloudFormation expression
(in which case the returned components will also be dynamic CloudFormation expressions,
encoded as Tokens).

###### `arn`<sup>Required</sup> <a name="arn" id="cdk-constructs.ThronStack.splitArn.parameter.arn"></a>

- *Type:* *string

the ARN to split into its components.

---

###### `arnFormat`<sup>Required</sup> <a name="arnFormat" id="cdk-constructs.ThronStack.splitArn.parameter.arnFormat"></a>

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.ArnFormat

the expected format of 'arn' - depends on what format the service 'arn' represents uses.

---

##### `ToJsonString` <a name="ToJsonString" id="cdk-constructs.ThronStack.toJsonString"></a>

```go
func ToJsonString(obj interface{}, space *f64) *string
```

Convert an object, potentially containing tokens, to a JSON string.

###### `obj`<sup>Required</sup> <a name="obj" id="cdk-constructs.ThronStack.toJsonString.parameter.obj"></a>

- *Type:* interface{}

---

###### `space`<sup>Optional</sup> <a name="space" id="cdk-constructs.ThronStack.toJsonString.parameter.space"></a>

- *Type:* *f64

---

##### `ToYamlString` <a name="ToYamlString" id="cdk-constructs.ThronStack.toYamlString"></a>

```go
func ToYamlString(obj interface{}) *string
```

Convert an object, potentially containing tokens, to a YAML string.

###### `obj`<sup>Required</sup> <a name="obj" id="cdk-constructs.ThronStack.toYamlString.parameter.obj"></a>

- *Type:* interface{}

---

#### Static Functions <a name="Static Functions" id="Static Functions"></a>

| **Name** | **Description** |
| --- | --- |
| <code><a href="#cdk-constructs.ThronStack.isConstruct">IsConstruct</a></code> | Checks if `x` is a construct. |
| <code><a href="#cdk-constructs.ThronStack.isStack">IsStack</a></code> | Return whether the given object is a Stack. |
| <code><a href="#cdk-constructs.ThronStack.of">Of</a></code> | Looks up the first stack scope in which `construct` is defined. |

---

##### `IsConstruct` <a name="IsConstruct" id="cdk-constructs.ThronStack.isConstruct"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

cdkconstructs.ThronStack_IsConstruct(x interface{}) *bool
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

- *Type:* interface{}

Any object.

---

##### `IsStack` <a name="IsStack" id="cdk-constructs.ThronStack.isStack"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

cdkconstructs.ThronStack_IsStack(x interface{}) *bool
```

Return whether the given object is a Stack.

We do attribute detection since we can't reliably use 'instanceof'.

###### `x`<sup>Required</sup> <a name="x" id="cdk-constructs.ThronStack.isStack.parameter.x"></a>

- *Type:* interface{}

---

##### `Of` <a name="Of" id="cdk-constructs.ThronStack.of"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

cdkconstructs.ThronStack_Of(construct IConstruct) Stack
```

Looks up the first stack scope in which `construct` is defined.

Fails if there is no stack up the tree.

###### `construct`<sup>Required</sup> <a name="construct" id="cdk-constructs.ThronStack.of.parameter.construct"></a>

- *Type:* github.com/aws/constructs-go/constructs/v10.IConstruct

The construct to start the search from.

---

#### Properties <a name="Properties" id="Properties"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.ThronStack.property.node">Node</a></code> | <code>github.com/aws/constructs-go/constructs/v10.Node</code> | The tree node. |
| <code><a href="#cdk-constructs.ThronStack.property.account">Account</a></code> | <code>*string</code> | The AWS account into which this stack will be deployed. |
| <code><a href="#cdk-constructs.ThronStack.property.artifactId">ArtifactId</a></code> | <code>*string</code> | The ID of the cloud assembly artifact for this stack. |
| <code><a href="#cdk-constructs.ThronStack.property.availabilityZones">AvailabilityZones</a></code> | <code>*[]*string</code> | Returns the list of AZs that are available in the AWS environment (account/region) associated with this stack. |
| <code><a href="#cdk-constructs.ThronStack.property.bundlingRequired">BundlingRequired</a></code> | <code>*bool</code> | Indicates whether the stack requires bundling or not. |
| <code><a href="#cdk-constructs.ThronStack.property.dependencies">Dependencies</a></code> | <code>*[]github.com/aws/aws-cdk-go/awscdk/v2.Stack</code> | Return the stacks this stack depends on. |
| <code><a href="#cdk-constructs.ThronStack.property.environment">Environment</a></code> | <code>*string</code> | The environment coordinates in which this stack is deployed. |
| <code><a href="#cdk-constructs.ThronStack.property.nested">Nested</a></code> | <code>*bool</code> | Indicates if this is a nested stack, in which case `parentStack` will include a reference to it's parent. |
| <code><a href="#cdk-constructs.ThronStack.property.notificationArns">NotificationArns</a></code> | <code>*[]*string</code> | Returns the list of notification Amazon Resource Names (ARNs) for the current stack. |
| <code><a href="#cdk-constructs.ThronStack.property.partition">Partition</a></code> | <code>*string</code> | The partition in which this stack is defined. |
| <code><a href="#cdk-constructs.ThronStack.property.region">Region</a></code> | <code>*string</code> | The AWS region into which this stack will be deployed (e.g. `us-west-2`). |
| <code><a href="#cdk-constructs.ThronStack.property.stackId">StackId</a></code> | <code>*string</code> | The ID of the stack. |
| <code><a href="#cdk-constructs.ThronStack.property.stackName">StackName</a></code> | <code>*string</code> | The concrete CloudFormation physical stack name. |
| <code><a href="#cdk-constructs.ThronStack.property.synthesizer">Synthesizer</a></code> | <code>github.com/aws/aws-cdk-go/awscdk/v2.IStackSynthesizer</code> | Synthesis method for this stack. |
| <code><a href="#cdk-constructs.ThronStack.property.tags">Tags</a></code> | <code>github.com/aws/aws-cdk-go/awscdk/v2.TagManager</code> | Tags to be applied to the stack. |
| <code><a href="#cdk-constructs.ThronStack.property.templateFile">TemplateFile</a></code> | <code>*string</code> | The name of the CloudFormation template file emitted to the output directory during synthesis. |
| <code><a href="#cdk-constructs.ThronStack.property.templateOptions">TemplateOptions</a></code> | <code>github.com/aws/aws-cdk-go/awscdk/v2.ITemplateOptions</code> | Options for CloudFormation template (like version, transform, description). |
| <code><a href="#cdk-constructs.ThronStack.property.urlSuffix">UrlSuffix</a></code> | <code>*string</code> | The Amazon domain suffix for the region in which this stack is defined. |
| <code><a href="#cdk-constructs.ThronStack.property.nestedStackParent">NestedStackParent</a></code> | <code>github.com/aws/aws-cdk-go/awscdk/v2.Stack</code> | If this is a nested stack, returns it's parent stack. |
| <code><a href="#cdk-constructs.ThronStack.property.nestedStackResource">NestedStackResource</a></code> | <code>github.com/aws/aws-cdk-go/awscdk/v2.CfnResource</code> | If this is a nested stack, this represents its `AWS::CloudFormation::Stack` resource. |
| <code><a href="#cdk-constructs.ThronStack.property.terminationProtection">TerminationProtection</a></code> | <code>*bool</code> | Whether termination protection is enabled for this stack. |
| <code><a href="#cdk-constructs.ThronStack.property.defaultValue">DefaultValue</a></code> | <code><a href="#cdk-constructs.DefaultValue">DefaultValue</a></code> | *No description.* |
| <code><a href="#cdk-constructs.ThronStack.property.projectId">ProjectId</a></code> | <code>*string</code> | *No description.* |
| <code><a href="#cdk-constructs.ThronStack.property.thronEnvironment">ThronEnvironment</a></code> | <code>*string</code> | *No description.* |
| <code><a href="#cdk-constructs.ThronStack.property.thronSitename">ThronSitename</a></code> | <code>*string</code> | *No description.* |

---

##### `Node`<sup>Required</sup> <a name="Node" id="cdk-constructs.ThronStack.property.node"></a>

```go
func Node() Node
```

- *Type:* github.com/aws/constructs-go/constructs/v10.Node

The tree node.

---

##### `Account`<sup>Required</sup> <a name="Account" id="cdk-constructs.ThronStack.property.account"></a>

```go
func Account() *string
```

- *Type:* *string

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

##### `ArtifactId`<sup>Required</sup> <a name="ArtifactId" id="cdk-constructs.ThronStack.property.artifactId"></a>

```go
func ArtifactId() *string
```

- *Type:* *string

The ID of the cloud assembly artifact for this stack.

---

##### `AvailabilityZones`<sup>Required</sup> <a name="AvailabilityZones" id="cdk-constructs.ThronStack.property.availabilityZones"></a>

```go
func AvailabilityZones() *[]*string
```

- *Type:* *[]*string

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

##### `BundlingRequired`<sup>Required</sup> <a name="BundlingRequired" id="cdk-constructs.ThronStack.property.bundlingRequired"></a>

```go
func BundlingRequired() *bool
```

- *Type:* *bool

Indicates whether the stack requires bundling or not.

---

##### `Dependencies`<sup>Required</sup> <a name="Dependencies" id="cdk-constructs.ThronStack.property.dependencies"></a>

```go
func Dependencies() *[]Stack
```

- *Type:* *[]github.com/aws/aws-cdk-go/awscdk/v2.Stack

Return the stacks this stack depends on.

---

##### `Environment`<sup>Required</sup> <a name="Environment" id="cdk-constructs.ThronStack.property.environment"></a>

```go
func Environment() *string
```

- *Type:* *string

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

##### `Nested`<sup>Required</sup> <a name="Nested" id="cdk-constructs.ThronStack.property.nested"></a>

```go
func Nested() *bool
```

- *Type:* *bool

Indicates if this is a nested stack, in which case `parentStack` will include a reference to it's parent.

---

##### `NotificationArns`<sup>Required</sup> <a name="NotificationArns" id="cdk-constructs.ThronStack.property.notificationArns"></a>

```go
func NotificationArns() *[]*string
```

- *Type:* *[]*string

Returns the list of notification Amazon Resource Names (ARNs) for the current stack.

---

##### `Partition`<sup>Required</sup> <a name="Partition" id="cdk-constructs.ThronStack.property.partition"></a>

```go
func Partition() *string
```

- *Type:* *string

The partition in which this stack is defined.

---

##### `Region`<sup>Required</sup> <a name="Region" id="cdk-constructs.ThronStack.property.region"></a>

```go
func Region() *string
```

- *Type:* *string

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

##### `StackId`<sup>Required</sup> <a name="StackId" id="cdk-constructs.ThronStack.property.stackId"></a>

```go
func StackId() *string
```

- *Type:* *string

The ID of the stack.

---

*Example*

```go
// After resolving, looks like
'arn:aws:cloudformation:us-west-2:123456789012:stack/teststack/51af3dc0-da77-11e4-872e-1234567db123'
```


##### `StackName`<sup>Required</sup> <a name="StackName" id="cdk-constructs.ThronStack.property.stackName"></a>

```go
func StackName() *string
```

- *Type:* *string

The concrete CloudFormation physical stack name.

This is either the name defined explicitly in the `stackName` prop or
allocated based on the stack's location in the construct tree. Stacks that
are directly defined under the app use their construct `id` as their stack
name. Stacks that are defined deeper within the tree will use a hashed naming
scheme based on the construct path to ensure uniqueness.

If you wish to obtain the deploy-time AWS::StackName intrinsic,
you can use `Aws.STACK_NAME` directly.

---

##### `Synthesizer`<sup>Required</sup> <a name="Synthesizer" id="cdk-constructs.ThronStack.property.synthesizer"></a>

```go
func Synthesizer() IStackSynthesizer
```

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.IStackSynthesizer

Synthesis method for this stack.

---

##### `Tags`<sup>Required</sup> <a name="Tags" id="cdk-constructs.ThronStack.property.tags"></a>

```go
func Tags() TagManager
```

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.TagManager

Tags to be applied to the stack.

---

##### `TemplateFile`<sup>Required</sup> <a name="TemplateFile" id="cdk-constructs.ThronStack.property.templateFile"></a>

```go
func TemplateFile() *string
```

- *Type:* *string

The name of the CloudFormation template file emitted to the output directory during synthesis.

Example value: `MyStack.template.json`

---

##### `TemplateOptions`<sup>Required</sup> <a name="TemplateOptions" id="cdk-constructs.ThronStack.property.templateOptions"></a>

```go
func TemplateOptions() ITemplateOptions
```

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.ITemplateOptions

Options for CloudFormation template (like version, transform, description).

---

##### `UrlSuffix`<sup>Required</sup> <a name="UrlSuffix" id="cdk-constructs.ThronStack.property.urlSuffix"></a>

```go
func UrlSuffix() *string
```

- *Type:* *string

The Amazon domain suffix for the region in which this stack is defined.

---

##### `NestedStackParent`<sup>Optional</sup> <a name="NestedStackParent" id="cdk-constructs.ThronStack.property.nestedStackParent"></a>

```go
func NestedStackParent() Stack
```

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.Stack

If this is a nested stack, returns it's parent stack.

---

##### `NestedStackResource`<sup>Optional</sup> <a name="NestedStackResource" id="cdk-constructs.ThronStack.property.nestedStackResource"></a>

```go
func NestedStackResource() CfnResource
```

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.CfnResource

If this is a nested stack, this represents its `AWS::CloudFormation::Stack` resource.

`undefined` for top-level (non-nested) stacks.

---

##### `TerminationProtection`<sup>Required</sup> <a name="TerminationProtection" id="cdk-constructs.ThronStack.property.terminationProtection"></a>

```go
func TerminationProtection() *bool
```

- *Type:* *bool

Whether termination protection is enabled for this stack.

---

##### `DefaultValue`<sup>Required</sup> <a name="DefaultValue" id="cdk-constructs.ThronStack.property.defaultValue"></a>

```go
func DefaultValue() DefaultValue
```

- *Type:* <a href="#cdk-constructs.DefaultValue">DefaultValue</a>

---

##### `ProjectId`<sup>Required</sup> <a name="ProjectId" id="cdk-constructs.ThronStack.property.projectId"></a>

```go
func ProjectId() *string
```

- *Type:* *string

---

##### `ThronEnvironment`<sup>Required</sup> <a name="ThronEnvironment" id="cdk-constructs.ThronStack.property.thronEnvironment"></a>

```go
func ThronEnvironment() *string
```

- *Type:* *string

---

##### `ThronSitename`<sup>Required</sup> <a name="ThronSitename" id="cdk-constructs.ThronStack.property.thronSitename"></a>

```go
func ThronSitename() *string
```

- *Type:* *string

---


### ThronTargetScaling <a name="ThronTargetScaling" id="cdk-constructs.ThronTargetScaling"></a>

#### Initializers <a name="Initializers" id="cdk-constructs.ThronTargetScaling.Initializer"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

cdkconstructs.NewThronTargetScaling(scope Construct, id *string, props ThronTargetScalingProps) ThronTargetScaling
```

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.ThronTargetScaling.Initializer.parameter.scope">scope</a></code> | <code>github.com/aws/constructs-go/constructs/v10.Construct</code> | *No description.* |
| <code><a href="#cdk-constructs.ThronTargetScaling.Initializer.parameter.id">id</a></code> | <code>*string</code> | *No description.* |
| <code><a href="#cdk-constructs.ThronTargetScaling.Initializer.parameter.props">props</a></code> | <code><a href="#cdk-constructs.ThronTargetScalingProps">ThronTargetScalingProps</a></code> | *No description.* |

---

##### `scope`<sup>Required</sup> <a name="scope" id="cdk-constructs.ThronTargetScaling.Initializer.parameter.scope"></a>

- *Type:* github.com/aws/constructs-go/constructs/v10.Construct

---

##### `id`<sup>Required</sup> <a name="id" id="cdk-constructs.ThronTargetScaling.Initializer.parameter.id"></a>

- *Type:* *string

---

##### `props`<sup>Required</sup> <a name="props" id="cdk-constructs.ThronTargetScaling.Initializer.parameter.props"></a>

- *Type:* <a href="#cdk-constructs.ThronTargetScalingProps">ThronTargetScalingProps</a>

---

#### Methods <a name="Methods" id="Methods"></a>

| **Name** | **Description** |
| --- | --- |
| <code><a href="#cdk-constructs.ThronTargetScaling.toString">ToString</a></code> | Returns a string representation of this construct. |

---

##### `ToString` <a name="ToString" id="cdk-constructs.ThronTargetScaling.toString"></a>

```go
func ToString() *string
```

Returns a string representation of this construct.

#### Static Functions <a name="Static Functions" id="Static Functions"></a>

| **Name** | **Description** |
| --- | --- |
| <code><a href="#cdk-constructs.ThronTargetScaling.isConstruct">IsConstruct</a></code> | Checks if `x` is a construct. |

---

##### `IsConstruct` <a name="IsConstruct" id="cdk-constructs.ThronTargetScaling.isConstruct"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

cdkconstructs.ThronTargetScaling_IsConstruct(x interface{}) *bool
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

- *Type:* interface{}

Any object.

---

#### Properties <a name="Properties" id="Properties"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.ThronTargetScaling.property.node">Node</a></code> | <code>github.com/aws/constructs-go/constructs/v10.Node</code> | The tree node. |
| <code><a href="#cdk-constructs.ThronTargetScaling.property.maxCapacity">MaxCapacity</a></code> | <code>*f64</code> | The maximum value that Application Auto Scaling can use to scale a target during a scaling activity. |
| <code><a href="#cdk-constructs.ThronTargetScaling.property.minCapacity">MinCapacity</a></code> | <code>*f64</code> | The minimum value that Application Auto Scaling can use to scale a target during a scaling activity. |
| <code><a href="#cdk-constructs.ThronTargetScaling.property.targetValue">TargetValue</a></code> | <code>*f64</code> | The target value for the metric. |
| <code><a href="#cdk-constructs.ThronTargetScaling.property.predefinedMetric">PredefinedMetric</a></code> | <code>github.com/aws/aws-cdk-go/awscdk/v2.aws_applicationautoscaling.PredefinedMetric</code> | A predefined metric for application autoscaling. |

---

##### `Node`<sup>Required</sup> <a name="Node" id="cdk-constructs.ThronTargetScaling.property.node"></a>

```go
func Node() Node
```

- *Type:* github.com/aws/constructs-go/constructs/v10.Node

The tree node.

---

##### `MaxCapacity`<sup>Required</sup> <a name="MaxCapacity" id="cdk-constructs.ThronTargetScaling.property.maxCapacity"></a>

```go
func MaxCapacity() *f64
```

- *Type:* *f64

The maximum value that Application Auto Scaling can use to scale a target during a scaling activity.

---

##### `MinCapacity`<sup>Required</sup> <a name="MinCapacity" id="cdk-constructs.ThronTargetScaling.property.minCapacity"></a>

```go
func MinCapacity() *f64
```

- *Type:* *f64

The minimum value that Application Auto Scaling can use to scale a target during a scaling activity.

---

##### `TargetValue`<sup>Required</sup> <a name="TargetValue" id="cdk-constructs.ThronTargetScaling.property.targetValue"></a>

```go
func TargetValue() *f64
```

- *Type:* *f64

The target value for the metric.

---

##### `PredefinedMetric`<sup>Optional</sup> <a name="PredefinedMetric" id="cdk-constructs.ThronTargetScaling.property.predefinedMetric"></a>

```go
func PredefinedMetric() PredefinedMetric
```

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_applicationautoscaling.PredefinedMetric

A predefined metric for application autoscaling.

The metric must track utilization. Scaling out will happen if the metric is higher than the target value,
scaling in will happen in the metric is lower than the target value.

---


### ThronVpc <a name="ThronVpc" id="cdk-constructs.ThronVpc"></a>

Construct for creating a DualsStack VPC with support for: - Dualstack - Vpc Endpoints - Vpc Peering - ... and many more.

More on the architecture here:
https://thron.atlassian.net/wiki/spaces/PPI/pages/1132888071/New+Network+Infrastructure+Proposal

*Example*

```go
// Example automatically generated from non-compiling source. May contain errors.
vpc := NewThronVpc(this, jsii.String("prova"), map[string]interface{}{
	"ipv4Cidr": jsii.String("10.8.0.0/16"),
	"isNatHA": jsii.Boolean(false),
	"prefix": jsii.String("prova"),
	"gatewayEndpoints": []interface{}{
		GatewayVpcEndpointAwsService_S3,
	},
	"interfaceEndpoints": []interface{}{
		InterfaceVpcEndpointAwsService_EC2,
	},
	"subnetsConfigs": []map[string]interface{}{
		map[string]interface{}{
			"availabilityZone": AvailabilityZone_A,
			"ipv4Cidr": jsii.String("10.8.192.0/20"),
			"ipv6CidrSlotNumber": jsii.Number(7),
			"type": SubnetType_PUBLIC,
		},
		map[string]interface{}{
			"availabilityZone": AvailabilityZone_B,
			"ipv4Cidr": jsii.String("10.8.208.0/20"),
			"ipv6CidrSlotNumber": jsii.Number(8),
			"type": SubnetType_PUBLIC,
		},
		map[string]interface{}{
			"availabilityZone": AvailabilityZone_C,
			"ipv4Cidr": jsii.String("10.8.224.0/20"),
			"ipv6CidrSlotNumber": jsii.Number(9),
			"type": SubnetType_PUBLIC,
		},
		map[string]interface{}{
			"availabilityZone": AvailabilityZone_A,
			"ipv4Cidr": jsii.String("10.8.0.0/18"),
			"ipv6CidrSlotNumber": jsii.Number(1),
			"type": SubnetType_PRIVATE,
		},
		map[string]interface{}{
			"availabilityZone": AvailabilityZone_B,
			"ipv4Cidr": jsii.String("10.8.64.0/18"),
			"ipv6CidrSlotNumber": jsii.Number(2),
			"type": SubnetType_PRIVATE,
		},
		map[string]interface{}{
			"availabilityZone": AvailabilityZone_C,
			"ipv4Cidr": jsii.String("10.8.128.0/18"),
			"ipv6CidrSlotNumber": jsii.Number(3),
			"type": SubnetType_PRIVATE,
		},
	},
})
```


#### Initializers <a name="Initializers" id="cdk-constructs.ThronVpc.Initializer"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

cdkconstructs.NewThronVpc(scope Construct, id *string, props ThronVpcProps) ThronVpc
```

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.ThronVpc.Initializer.parameter.scope">scope</a></code> | <code>github.com/aws/constructs-go/constructs/v10.Construct</code> | Construct on which to instantiate the VPC on. |
| <code><a href="#cdk-constructs.ThronVpc.Initializer.parameter.id">id</a></code> | <code>*string</code> | Logical id of the construct. |
| <code><a href="#cdk-constructs.ThronVpc.Initializer.parameter.props">props</a></code> | <code><a href="#cdk-constructs.ThronVpcProps">ThronVpcProps</a></code> | *No description.* |

---

##### `scope`<sup>Required</sup> <a name="scope" id="cdk-constructs.ThronVpc.Initializer.parameter.scope"></a>

- *Type:* github.com/aws/constructs-go/constructs/v10.Construct

Construct on which to instantiate the VPC on.

---

##### `id`<sup>Required</sup> <a name="id" id="cdk-constructs.ThronVpc.Initializer.parameter.id"></a>

- *Type:* *string

Logical id of the construct.

---

##### `props`<sup>Required</sup> <a name="props" id="cdk-constructs.ThronVpc.Initializer.parameter.props"></a>

- *Type:* <a href="#cdk-constructs.ThronVpcProps">ThronVpcProps</a>

---

#### Methods <a name="Methods" id="Methods"></a>

| **Name** | **Description** |
| --- | --- |
| <code><a href="#cdk-constructs.ThronVpc.toString">ToString</a></code> | Returns a string representation of this construct. |
| <code><a href="#cdk-constructs.ThronVpc.addAtlasClusterPeering">AddAtlasClusterPeering</a></code> | *No description.* |
| <code><a href="#cdk-constructs.ThronVpc.addPeeringFromOtherAccount">AddPeeringFromOtherAccount</a></code> | Adds a peering with another VPC in another account, along with the routes. |
| <code><a href="#cdk-constructs.ThronVpc.addVpcPeering">AddVpcPeering</a></code> | Adds a peering with another VPC, along with the routes. |

---

##### `ToString` <a name="ToString" id="cdk-constructs.ThronVpc.toString"></a>

```go
func ToString() *string
```

Returns a string representation of this construct.

##### `AddAtlasClusterPeering` <a name="AddAtlasClusterPeering" id="cdk-constructs.ThronVpc.addAtlasClusterPeering"></a>

```go
func AddAtlasClusterPeering(peeringConf AtlasPeeringConf) *string
```

###### `peeringConf`<sup>Required</sup> <a name="peeringConf" id="cdk-constructs.ThronVpc.addAtlasClusterPeering.parameter.peeringConf"></a>

- *Type:* <a href="#cdk-constructs.AtlasPeeringConf">AtlasPeeringConf</a>

Configuration for the atlas peering.

---

##### `AddPeeringFromOtherAccount` <a name="AddPeeringFromOtherAccount" id="cdk-constructs.ThronVpc.addPeeringFromOtherAccount"></a>

```go
func AddPeeringFromOtherAccount(peerConfig OtherAccountPeeringConfig) *string
```

Adds a peering with another VPC in another account, along with the routes.

###### `peerConfig`<sup>Required</sup> <a name="peerConfig" id="cdk-constructs.ThronVpc.addPeeringFromOtherAccount.parameter.peerConfig"></a>

- *Type:* <a href="#cdk-constructs.OtherAccountPeeringConfig">OtherAccountPeeringConfig</a>

Peering configuration.

---

##### `AddVpcPeering` <a name="AddVpcPeering" id="cdk-constructs.ThronVpc.addVpcPeering"></a>

```go
func AddVpcPeering(peerConfig PeeringConfig)
```

Adds a peering with another VPC, along with the routes.

###### `peerConfig`<sup>Required</sup> <a name="peerConfig" id="cdk-constructs.ThronVpc.addVpcPeering.parameter.peerConfig"></a>

- *Type:* <a href="#cdk-constructs.PeeringConfig">PeeringConfig</a>

Peering configuration.

---

#### Static Functions <a name="Static Functions" id="Static Functions"></a>

| **Name** | **Description** |
| --- | --- |
| <code><a href="#cdk-constructs.ThronVpc.isConstruct">IsConstruct</a></code> | Checks if `x` is a construct. |

---

##### `IsConstruct` <a name="IsConstruct" id="cdk-constructs.ThronVpc.isConstruct"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

cdkconstructs.ThronVpc_IsConstruct(x interface{}) *bool
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

- *Type:* interface{}

Any object.

---

#### Properties <a name="Properties" id="Properties"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.ThronVpc.property.node">Node</a></code> | <code>github.com/aws/constructs-go/constructs/v10.Node</code> | The tree node. |
| <code><a href="#cdk-constructs.ThronVpc.property.egressOnlyInternetGateway">EgressOnlyInternetGateway</a></code> | <code>github.com/aws/aws-cdk-go/awscdk/v2.aws_ec2.CfnEgressOnlyInternetGateway</code> | *No description.* |
| <code><a href="#cdk-constructs.ThronVpc.property.gatewayEndpoints">GatewayEndpoints</a></code> | <code>*[]github.com/aws/aws-cdk-go/awscdk/v2.aws_ec2.GatewayVpcEndpoint</code> | *No description.* |
| <code><a href="#cdk-constructs.ThronVpc.property.interfaceEndpoints">InterfaceEndpoints</a></code> | <code>*[]github.com/aws/aws-cdk-go/awscdk/v2.aws_ec2.InterfaceVpcEndpoint</code> | *No description.* |
| <code><a href="#cdk-constructs.ThronVpc.property.internetGateway">InternetGateway</a></code> | <code>github.com/aws/aws-cdk-go/awscdk/v2.aws_ec2.CfnInternetGateway</code> | *No description.* |
| <code><a href="#cdk-constructs.ThronVpc.property.ipv4CidrBlock">Ipv4CidrBlock</a></code> | <code>*string</code> | *No description.* |
| <code><a href="#cdk-constructs.ThronVpc.property.ipv6CidrBlock">Ipv6CidrBlock</a></code> | <code>*string</code> | *No description.* |
| <code><a href="#cdk-constructs.ThronVpc.property.nats">Nats</a></code> | <code>*[]github.com/aws/aws-cdk-go/awscdk/v2.aws_ec2.CfnNatGateway</code> | *No description.* |
| <code><a href="#cdk-constructs.ThronVpc.property.prefix">Prefix</a></code> | <code>*string</code> | *No description.* |
| <code><a href="#cdk-constructs.ThronVpc.property.privateSubnets">PrivateSubnets</a></code> | <code>*[]github.com/aws/aws-cdk-go/awscdk/v2.aws_ec2.Subnet</code> | *No description.* |
| <code><a href="#cdk-constructs.ThronVpc.property.publicSubnets">PublicSubnets</a></code> | <code>*[]github.com/aws/aws-cdk-go/awscdk/v2.aws_ec2.Subnet</code> | *No description.* |
| <code><a href="#cdk-constructs.ThronVpc.property.vpc">Vpc</a></code> | <code>github.com/aws/aws-cdk-go/awscdk/v2.aws_ec2.Vpc</code> | *No description.* |

---

##### `Node`<sup>Required</sup> <a name="Node" id="cdk-constructs.ThronVpc.property.node"></a>

```go
func Node() Node
```

- *Type:* github.com/aws/constructs-go/constructs/v10.Node

The tree node.

---

##### `EgressOnlyInternetGateway`<sup>Required</sup> <a name="EgressOnlyInternetGateway" id="cdk-constructs.ThronVpc.property.egressOnlyInternetGateway"></a>

```go
func EgressOnlyInternetGateway() CfnEgressOnlyInternetGateway
```

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_ec2.CfnEgressOnlyInternetGateway

---

##### `GatewayEndpoints`<sup>Required</sup> <a name="GatewayEndpoints" id="cdk-constructs.ThronVpc.property.gatewayEndpoints"></a>

```go
func GatewayEndpoints() *[]GatewayVpcEndpoint
```

- *Type:* *[]github.com/aws/aws-cdk-go/awscdk/v2.aws_ec2.GatewayVpcEndpoint

---

##### `InterfaceEndpoints`<sup>Required</sup> <a name="InterfaceEndpoints" id="cdk-constructs.ThronVpc.property.interfaceEndpoints"></a>

```go
func InterfaceEndpoints() *[]InterfaceVpcEndpoint
```

- *Type:* *[]github.com/aws/aws-cdk-go/awscdk/v2.aws_ec2.InterfaceVpcEndpoint

---

##### `InternetGateway`<sup>Required</sup> <a name="InternetGateway" id="cdk-constructs.ThronVpc.property.internetGateway"></a>

```go
func InternetGateway() CfnInternetGateway
```

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_ec2.CfnInternetGateway

---

##### `Ipv4CidrBlock`<sup>Required</sup> <a name="Ipv4CidrBlock" id="cdk-constructs.ThronVpc.property.ipv4CidrBlock"></a>

```go
func Ipv4CidrBlock() *string
```

- *Type:* *string

---

##### `Ipv6CidrBlock`<sup>Required</sup> <a name="Ipv6CidrBlock" id="cdk-constructs.ThronVpc.property.ipv6CidrBlock"></a>

```go
func Ipv6CidrBlock() *string
```

- *Type:* *string

---

##### `Nats`<sup>Required</sup> <a name="Nats" id="cdk-constructs.ThronVpc.property.nats"></a>

```go
func Nats() *[]CfnNatGateway
```

- *Type:* *[]github.com/aws/aws-cdk-go/awscdk/v2.aws_ec2.CfnNatGateway

---

##### `Prefix`<sup>Required</sup> <a name="Prefix" id="cdk-constructs.ThronVpc.property.prefix"></a>

```go
func Prefix() *string
```

- *Type:* *string

---

##### `PrivateSubnets`<sup>Required</sup> <a name="PrivateSubnets" id="cdk-constructs.ThronVpc.property.privateSubnets"></a>

```go
func PrivateSubnets() *[]Subnet
```

- *Type:* *[]github.com/aws/aws-cdk-go/awscdk/v2.aws_ec2.Subnet

---

##### `PublicSubnets`<sup>Required</sup> <a name="PublicSubnets" id="cdk-constructs.ThronVpc.property.publicSubnets"></a>

```go
func PublicSubnets() *[]Subnet
```

- *Type:* *[]github.com/aws/aws-cdk-go/awscdk/v2.aws_ec2.Subnet

---

##### `Vpc`<sup>Required</sup> <a name="Vpc" id="cdk-constructs.ThronVpc.property.vpc"></a>

```go
func Vpc() Vpc
```

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_ec2.Vpc

---


## Structs <a name="Structs" id="Structs"></a>

### AtlasPeeringConf <a name="AtlasPeeringConf" id="cdk-constructs.AtlasPeeringConf"></a>

#### Initializer <a name="Initializer" id="cdk-constructs.AtlasPeeringConf.Initializer"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

&cdkconstructs.AtlasPeeringConf {
	AtlasCidr: *string,
	AtlasContainerId: *string,
	AtlasProjectId: *string,
	ClusterName: *string,
}
```

#### Properties <a name="Properties" id="Properties"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.AtlasPeeringConf.property.atlasCidr">AtlasCidr</a></code> | <code>*string</code> | Cidr notation of the atlas cluster. |
| <code><a href="#cdk-constructs.AtlasPeeringConf.property.atlasContainerId">AtlasContainerId</a></code> | <code>*string</code> | Id of the atlas network container. |
| <code><a href="#cdk-constructs.AtlasPeeringConf.property.atlasProjectId">AtlasProjectId</a></code> | <code>*string</code> | Id of the atlas project. |
| <code><a href="#cdk-constructs.AtlasPeeringConf.property.clusterName">ClusterName</a></code> | <code>*string</code> | Name of the cluster to be used as logical di. |

---

##### `AtlasCidr`<sup>Required</sup> <a name="AtlasCidr" id="cdk-constructs.AtlasPeeringConf.property.atlasCidr"></a>

```go
AtlasCidr *string
```

- *Type:* *string

Cidr notation of the atlas cluster.

---

##### `AtlasContainerId`<sup>Required</sup> <a name="AtlasContainerId" id="cdk-constructs.AtlasPeeringConf.property.atlasContainerId"></a>

```go
AtlasContainerId *string
```

- *Type:* *string

Id of the atlas network container.

---

##### `AtlasProjectId`<sup>Required</sup> <a name="AtlasProjectId" id="cdk-constructs.AtlasPeeringConf.property.atlasProjectId"></a>

```go
AtlasProjectId *string
```

- *Type:* *string

Id of the atlas project.

---

##### `ClusterName`<sup>Required</sup> <a name="ClusterName" id="cdk-constructs.AtlasPeeringConf.property.clusterName"></a>

```go
ClusterName *string
```

- *Type:* *string

Name of the cluster to be used as logical di.

---

### CicdEnvironment <a name="CicdEnvironment" id="cdk-constructs.CicdEnvironment"></a>

#### Initializer <a name="Initializer" id="cdk-constructs.CicdEnvironment.Initializer"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

&cdkconstructs.CicdEnvironment {
	Capabilities: *[]git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs.PipelineCapability,
	WebhookUrl: *string,
}
```

#### Properties <a name="Properties" id="Properties"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.CicdEnvironment.property.capabilities">Capabilities</a></code> | <code>*[]<a href="#cdk-constructs.PipelineCapability">PipelineCapability</a></code> | *No description.* |
| <code><a href="#cdk-constructs.CicdEnvironment.property.webhookUrl">WebhookUrl</a></code> | <code>*string</code> | *No description.* |

---

##### `Capabilities`<sup>Required</sup> <a name="Capabilities" id="cdk-constructs.CicdEnvironment.property.capabilities"></a>

```go
Capabilities *[]PipelineCapability
```

- *Type:* *[]<a href="#cdk-constructs.PipelineCapability">PipelineCapability</a>

---

##### `WebhookUrl`<sup>Optional</sup> <a name="WebhookUrl" id="cdk-constructs.CicdEnvironment.property.webhookUrl"></a>

```go
WebhookUrl *string
```

- *Type:* *string

---

### DeployConfig <a name="DeployConfig" id="cdk-constructs.DeployConfig"></a>

#### Initializer <a name="Initializer" id="cdk-constructs.DeployConfig.Initializer"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

&cdkconstructs.DeployConfig {
	DeploymentAwsAccount: *string,
	DeploymentAwsRegion: *string,
	DeploymentEnvironment: *string,
	DeploymentSitename: *string,
	ProjectId: *string,
}
```

#### Properties <a name="Properties" id="Properties"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.DeployConfig.property.deploymentAwsAccount">DeploymentAwsAccount</a></code> | <code>*string</code> | *No description.* |
| <code><a href="#cdk-constructs.DeployConfig.property.deploymentAwsRegion">DeploymentAwsRegion</a></code> | <code>*string</code> | *No description.* |
| <code><a href="#cdk-constructs.DeployConfig.property.deploymentEnvironment">DeploymentEnvironment</a></code> | <code>*string</code> | *No description.* |
| <code><a href="#cdk-constructs.DeployConfig.property.deploymentSitename">DeploymentSitename</a></code> | <code>*string</code> | *No description.* |
| <code><a href="#cdk-constructs.DeployConfig.property.projectId">ProjectId</a></code> | <code>*string</code> | *No description.* |

---

##### `DeploymentAwsAccount`<sup>Required</sup> <a name="DeploymentAwsAccount" id="cdk-constructs.DeployConfig.property.deploymentAwsAccount"></a>

```go
DeploymentAwsAccount *string
```

- *Type:* *string

---

##### `DeploymentAwsRegion`<sup>Required</sup> <a name="DeploymentAwsRegion" id="cdk-constructs.DeployConfig.property.deploymentAwsRegion"></a>

```go
DeploymentAwsRegion *string
```

- *Type:* *string

---

##### `DeploymentEnvironment`<sup>Required</sup> <a name="DeploymentEnvironment" id="cdk-constructs.DeployConfig.property.deploymentEnvironment"></a>

```go
DeploymentEnvironment *string
```

- *Type:* *string

---

##### `DeploymentSitename`<sup>Required</sup> <a name="DeploymentSitename" id="cdk-constructs.DeployConfig.property.deploymentSitename"></a>

```go
DeploymentSitename *string
```

- *Type:* *string

---

##### `ProjectId`<sup>Required</sup> <a name="ProjectId" id="cdk-constructs.DeployConfig.property.projectId"></a>

```go
ProjectId *string
```

- *Type:* *string

---

### DeployStepConf <a name="DeployStepConf" id="cdk-constructs.DeployStepConf"></a>

#### Initializer <a name="Initializer" id="cdk-constructs.DeployStepConf.Initializer"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

&cdkconstructs.DeployStepConf {
	ComputeType: github.com/aws/aws-cdk-go/awscdk/v2.aws_codebuild.ComputeType,
	CustomBuildImage: github.com/aws/aws-cdk-go/awscdk/v2.aws_codebuild.IBuildImage,
	EnvironmentalVariables: *map[string]github.com/aws/aws-cdk-go/awscdk/v2.aws_codebuild.BuildEnvironmentVariable,
	EnvironmentConf: git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs.DeployConfig,
}
```

#### Properties <a name="Properties" id="Properties"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.DeployStepConf.property.computeType">ComputeType</a></code> | <code>github.com/aws/aws-cdk-go/awscdk/v2.aws_codebuild.ComputeType</code> | Specify the size of the build containers. See https://docs.aws.amazon.com/codebuild/latest/userguide/build-env-ref-compute-types.html#environment.types for reference. |
| <code><a href="#cdk-constructs.DeployStepConf.property.customBuildImage">CustomBuildImage</a></code> | <code>github.com/aws/aws-cdk-go/awscdk/v2.aws_codebuild.IBuildImage</code> | Build image to be used fot this step. |
| <code><a href="#cdk-constructs.DeployStepConf.property.environmentalVariables">EnvironmentalVariables</a></code> | <code>*map[string]github.com/aws/aws-cdk-go/awscdk/v2.aws_codebuild.BuildEnvironmentVariable</code> | Map of additional env vars to pass to the build container. |
| <code><a href="#cdk-constructs.DeployStepConf.property.environmentConf">EnvironmentConf</a></code> | <code><a href="#cdk-constructs.DeployConfig">DeployConfig</a></code> | *No description.* |

---

##### `ComputeType`<sup>Optional</sup> <a name="ComputeType" id="cdk-constructs.DeployStepConf.property.computeType"></a>

```go
ComputeType ComputeType
```

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_codebuild.ComputeType

Specify the size of the build containers. See https://docs.aws.amazon.com/codebuild/latest/userguide/build-env-ref-compute-types.html#environment.types for reference.

Defaults to `ComputeType.SMALL`

---

##### `CustomBuildImage`<sup>Optional</sup> <a name="CustomBuildImage" id="cdk-constructs.DeployStepConf.property.customBuildImage"></a>

```go
CustomBuildImage IBuildImage
```

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_codebuild.IBuildImage

Build image to be used fot this step.

---

##### `EnvironmentalVariables`<sup>Optional</sup> <a name="EnvironmentalVariables" id="cdk-constructs.DeployStepConf.property.environmentalVariables"></a>

```go
EnvironmentalVariables *map[string]BuildEnvironmentVariable
```

- *Type:* *map[string]github.com/aws/aws-cdk-go/awscdk/v2.aws_codebuild.BuildEnvironmentVariable

Map of additional env vars to pass to the build container.

---

##### `EnvironmentConf`<sup>Required</sup> <a name="EnvironmentConf" id="cdk-constructs.DeployStepConf.property.environmentConf"></a>

```go
EnvironmentConf DeployConfig
```

- *Type:* <a href="#cdk-constructs.DeployConfig">DeployConfig</a>

---

### ECRDeploymentProps <a name="ECRDeploymentProps" id="cdk-constructs.ECRDeploymentProps"></a>

#### Initializer <a name="Initializer" id="cdk-constructs.ECRDeploymentProps.Initializer"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

&cdkconstructs.ECRDeploymentProps {
	Dest: git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs.IImageName,
	Src: git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs.IImageName,
	BuildImage: *string,
	Environment: *map[string]*string,
	MemoryLimit: *f64,
	Role: github.com/aws/aws-cdk-go/awscdk/v2.aws_iam.IRole,
	Vpc: github.com/aws/aws-cdk-go/awscdk/v2.aws_ec2.IVpc,
	VpcSubnets: github.com/aws/aws-cdk-go/awscdk/v2.aws_ec2.SubnetSelection,
}
```

#### Properties <a name="Properties" id="Properties"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.ECRDeploymentProps.property.dest">Dest</a></code> | <code><a href="#cdk-constructs.IImageName">IImageName</a></code> | The destination of the docker image. |
| <code><a href="#cdk-constructs.ECRDeploymentProps.property.src">Src</a></code> | <code><a href="#cdk-constructs.IImageName">IImageName</a></code> | The source of the docker image. |
| <code><a href="#cdk-constructs.ECRDeploymentProps.property.buildImage">BuildImage</a></code> | <code>*string</code> | Image to use to build Golang lambda for custom resource, if download fails or is not wanted. |
| <code><a href="#cdk-constructs.ECRDeploymentProps.property.environment">Environment</a></code> | <code>*map[string]*string</code> | The environment variable to set. |
| <code><a href="#cdk-constructs.ECRDeploymentProps.property.memoryLimit">MemoryLimit</a></code> | <code>*f64</code> | The amount of memory (in MiB) to allocate to the AWS Lambda function which replicates the files from the CDK bucket to the destination bucket. |
| <code><a href="#cdk-constructs.ECRDeploymentProps.property.role">Role</a></code> | <code>github.com/aws/aws-cdk-go/awscdk/v2.aws_iam.IRole</code> | Execution role associated with this function. |
| <code><a href="#cdk-constructs.ECRDeploymentProps.property.vpc">Vpc</a></code> | <code>github.com/aws/aws-cdk-go/awscdk/v2.aws_ec2.IVpc</code> | The VPC network to place the deployment lambda handler in. |
| <code><a href="#cdk-constructs.ECRDeploymentProps.property.vpcSubnets">VpcSubnets</a></code> | <code>github.com/aws/aws-cdk-go/awscdk/v2.aws_ec2.SubnetSelection</code> | Where in the VPC to place the deployment lambda handler. |

---

##### `Dest`<sup>Required</sup> <a name="Dest" id="cdk-constructs.ECRDeploymentProps.property.dest"></a>

```go
Dest IImageName
```

- *Type:* <a href="#cdk-constructs.IImageName">IImageName</a>

The destination of the docker image.

---

##### `Src`<sup>Required</sup> <a name="Src" id="cdk-constructs.ECRDeploymentProps.property.src"></a>

```go
Src IImageName
```

- *Type:* <a href="#cdk-constructs.IImageName">IImageName</a>

The source of the docker image.

---

##### `BuildImage`<sup>Optional</sup> <a name="BuildImage" id="cdk-constructs.ECRDeploymentProps.property.buildImage"></a>

```go
BuildImage *string
```

- *Type:* *string
- *Default:* public.ecr.aws/sam/build-go1.x:latest

Image to use to build Golang lambda for custom resource, if download fails or is not wanted.

Might be needed for local build if all images need to come from own registry.

Note that image should use yum as a package manager and have golang available.

---

##### `Environment`<sup>Optional</sup> <a name="Environment" id="cdk-constructs.ECRDeploymentProps.property.environment"></a>

```go
Environment *map[string]*string
```

- *Type:* *map[string]*string

The environment variable to set.

---

##### `MemoryLimit`<sup>Optional</sup> <a name="MemoryLimit" id="cdk-constructs.ECRDeploymentProps.property.memoryLimit"></a>

```go
MemoryLimit *f64
```

- *Type:* *f64
- *Default:* 512

The amount of memory (in MiB) to allocate to the AWS Lambda function which replicates the files from the CDK bucket to the destination bucket.

If you are deploying large files, you will need to increase this number
accordingly.

---

##### `Role`<sup>Optional</sup> <a name="Role" id="cdk-constructs.ECRDeploymentProps.property.role"></a>

```go
Role IRole
```

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_iam.IRole
- *Default:* A role is automatically created

Execution role associated with this function.

---

##### `Vpc`<sup>Optional</sup> <a name="Vpc" id="cdk-constructs.ECRDeploymentProps.property.vpc"></a>

```go
Vpc IVpc
```

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_ec2.IVpc
- *Default:* None

The VPC network to place the deployment lambda handler in.

---

##### `VpcSubnets`<sup>Optional</sup> <a name="VpcSubnets" id="cdk-constructs.ECRDeploymentProps.property.vpcSubnets"></a>

```go
VpcSubnets SubnetSelection
```

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_ec2.SubnetSelection
- *Default:* the Vpc default strategy if not specified

Where in the VPC to place the deployment lambda handler.

Only used if 'vpc' is supplied.

---

### EndpointComponents <a name="EndpointComponents" id="cdk-constructs.EndpointComponents"></a>

#### Initializer <a name="Initializer" id="cdk-constructs.EndpointComponents.Initializer"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

&cdkconstructs.EndpointComponents {
	Domain: *string,
	FullRecord: *string,
	Path: *string,
}
```

#### Properties <a name="Properties" id="Properties"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.EndpointComponents.property.domain">Domain</a></code> | <code>*string</code> | The domain part of the endpoint, i.e. `awsd04-product-api-adv1-productimports.4me.cdndev.weebo.it`. |
| <code><a href="#cdk-constructs.EndpointComponents.property.fullRecord">FullRecord</a></code> | <code>*string</code> | The full endpoint record, i.e. `awsd04-product-api-adv1-productimports.4me.cdndev.weebo.it/api/adv1/productimports/`. |
| <code><a href="#cdk-constructs.EndpointComponents.property.path">Path</a></code> | <code>*string</code> | The path of the endpoint, i.e. `/api/adv1/productimports/`. |

---

##### `Domain`<sup>Required</sup> <a name="Domain" id="cdk-constructs.EndpointComponents.property.domain"></a>

```go
Domain *string
```

- *Type:* *string

The domain part of the endpoint, i.e. `awsd04-product-api-adv1-productimports.4me.cdndev.weebo.it`.

---

##### `FullRecord`<sup>Required</sup> <a name="FullRecord" id="cdk-constructs.EndpointComponents.property.fullRecord"></a>

```go
FullRecord *string
```

- *Type:* *string

The full endpoint record, i.e. `awsd04-product-api-adv1-productimports.4me.cdndev.weebo.it/api/adv1/productimports/`.

---

##### `Path`<sup>Required</sup> <a name="Path" id="cdk-constructs.EndpointComponents.property.path"></a>

```go
Path *string
```

- *Type:* *string

The path of the endpoint, i.e. `/api/adv1/productimports/`.

---

### EnvironmentConfig <a name="EnvironmentConfig" id="cdk-constructs.EnvironmentConfig"></a>

#### Initializer <a name="Initializer" id="cdk-constructs.EnvironmentConfig.Initializer"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

&cdkconstructs.EnvironmentConfig {
	DeploymentAwsAccount: *string,
	DeploymentAwsRegion: *string,
	DeploymentEnvironment: *string,
	DeploymentSitename: *string,
}
```

#### Properties <a name="Properties" id="Properties"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.EnvironmentConfig.property.deploymentAwsAccount">DeploymentAwsAccount</a></code> | <code>*string</code> | *No description.* |
| <code><a href="#cdk-constructs.EnvironmentConfig.property.deploymentAwsRegion">DeploymentAwsRegion</a></code> | <code>*string</code> | *No description.* |
| <code><a href="#cdk-constructs.EnvironmentConfig.property.deploymentEnvironment">DeploymentEnvironment</a></code> | <code>*string</code> | *No description.* |
| <code><a href="#cdk-constructs.EnvironmentConfig.property.deploymentSitename">DeploymentSitename</a></code> | <code>*string</code> | *No description.* |

---

##### `DeploymentAwsAccount`<sup>Required</sup> <a name="DeploymentAwsAccount" id="cdk-constructs.EnvironmentConfig.property.deploymentAwsAccount"></a>

```go
DeploymentAwsAccount *string
```

- *Type:* *string

---

##### `DeploymentAwsRegion`<sup>Required</sup> <a name="DeploymentAwsRegion" id="cdk-constructs.EnvironmentConfig.property.deploymentAwsRegion"></a>

```go
DeploymentAwsRegion *string
```

- *Type:* *string

---

##### `DeploymentEnvironment`<sup>Required</sup> <a name="DeploymentEnvironment" id="cdk-constructs.EnvironmentConfig.property.deploymentEnvironment"></a>

```go
DeploymentEnvironment *string
```

- *Type:* *string

---

##### `DeploymentSitename`<sup>Required</sup> <a name="DeploymentSitename" id="cdk-constructs.EnvironmentConfig.property.deploymentSitename"></a>

```go
DeploymentSitename *string
```

- *Type:* *string

---

### FullServiceProps <a name="FullServiceProps" id="cdk-constructs.FullServiceProps"></a>

#### Initializer <a name="Initializer" id="cdk-constructs.FullServiceProps.Initializer"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

&cdkconstructs.FullServiceProps {
	ServiceGroup: git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs.ServiceGroup,
	Version: *f64,
	Visibility: git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs.EndpointVisibility,
	ServiceName: *string,
}
```

#### Properties <a name="Properties" id="Properties"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.FullServiceProps.property.serviceGroup">ServiceGroup</a></code> | <code><a href="#cdk-constructs.ServiceGroup">ServiceGroup</a></code> | Service group of the service. |
| <code><a href="#cdk-constructs.FullServiceProps.property.version">Version</a></code> | <code>*f64</code> | The version of the API exposed by the endpoint. |
| <code><a href="#cdk-constructs.FullServiceProps.property.visibility">Visibility</a></code> | <code><a href="#cdk-constructs.EndpointVisibility">EndpointVisibility</a></code> | Wether the endpoint is private or public. |
| <code><a href="#cdk-constructs.FullServiceProps.property.serviceName">ServiceName</a></code> | <code>*string</code> | Name of the service the endpoint exposes. |

---

##### `ServiceGroup`<sup>Required</sup> <a name="ServiceGroup" id="cdk-constructs.FullServiceProps.property.serviceGroup"></a>

```go
ServiceGroup ServiceGroup
```

- *Type:* <a href="#cdk-constructs.ServiceGroup">ServiceGroup</a>
- *Default:* ServiceGroup.VIEW

Service group of the service.

---

##### `Version`<sup>Required</sup> <a name="Version" id="cdk-constructs.FullServiceProps.property.version"></a>

```go
Version *f64
```

- *Type:* *f64
- *Default:* 1

The version of the API exposed by the endpoint.

---

##### `Visibility`<sup>Required</sup> <a name="Visibility" id="cdk-constructs.FullServiceProps.property.visibility"></a>

```go
Visibility EndpointVisibility
```

- *Type:* <a href="#cdk-constructs.EndpointVisibility">EndpointVisibility</a>
- *Default:* EndpointVisibility.PRIVATE

Wether the endpoint is private or public.

---

##### `ServiceName`<sup>Required</sup> <a name="ServiceName" id="cdk-constructs.FullServiceProps.property.serviceName"></a>

```go
ServiceName *string
```

- *Type:* *string

Name of the service the endpoint exposes.

---

### FunctionOptions <a name="FunctionOptions" id="cdk-constructs.FunctionOptions"></a>

#### Initializer <a name="Initializer" id="cdk-constructs.FunctionOptions.Initializer"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

&cdkconstructs.FunctionOptions {
	ApiGatewayEndpoints: *map[string]git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs.ThronLambdaApiGatewayEndpointProps,
	Architecture: github.com/aws/aws-cdk-go/awscdk/v2.aws_lambda.Architecture,
	AreMultiValueHeadersEnabled: *bool,
	Description: *string,
	DockerContextPath: *string,
	DockerfileName: *string,
	Endpoints: *map[string]git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs.ThronEndpointAlbProps,
	Environment: *map[string]*string,
	EphemeralStorageSize: github.com/aws/aws-cdk-go/awscdk/v2.Size,
	ExistingDockerImage: github.com/aws/aws-cdk-go/awscdk/v2.aws_lambda.DockerImageCode,
	Filesystem: github.com/aws/aws-cdk-go/awscdk/v2.aws_lambda.FileSystem,
	LegacyEndpoints: *map[string]git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs.LegacyEndpointAlbProps,
	MemorySize: *f64,
	ReservedConcurrentExecutions: *f64,
	Timeout: github.com/aws/aws-cdk-go/awscdk/v2.Duration,
}
```

#### Properties <a name="Properties" id="Properties"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.FunctionOptions.property.apiGatewayEndpoints">ApiGatewayEndpoints</a></code> | <code>*map[string]<a href="#cdk-constructs.ThronLambdaApiGatewayEndpointProps">ThronLambdaApiGatewayEndpointProps</a></code> | Api Gateway endpoints associated with this lambda. |
| <code><a href="#cdk-constructs.FunctionOptions.property.architecture">Architecture</a></code> | <code>github.com/aws/aws-cdk-go/awscdk/v2.aws_lambda.Architecture</code> | The architecture the lambda function runs on. |
| <code><a href="#cdk-constructs.FunctionOptions.property.areMultiValueHeadersEnabled">AreMultiValueHeadersEnabled</a></code> | <code>*bool</code> | Whether or not multi value headers are enabled. |
| <code><a href="#cdk-constructs.FunctionOptions.property.description">Description</a></code> | <code>*string</code> | A description of the function. |
| <code><a href="#cdk-constructs.FunctionOptions.property.dockerContextPath">DockerContextPath</a></code> | <code>*string</code> | Context of docker build. |
| <code><a href="#cdk-constructs.FunctionOptions.property.dockerfileName">DockerfileName</a></code> | <code>*string</code> | Name of Dockerfile. |
| <code><a href="#cdk-constructs.FunctionOptions.property.endpoints">Endpoints</a></code> | <code>*map[string]<a href="#cdk-constructs.ThronEndpointAlbProps">ThronEndpointAlbProps</a></code> | Endpoints associated with this lambda. |
| <code><a href="#cdk-constructs.FunctionOptions.property.environment">Environment</a></code> | <code>*map[string]*string</code> | Key-value pairs that Lambda caches and makes available for your Lambda functions. |
| <code><a href="#cdk-constructs.FunctionOptions.property.ephemeralStorageSize">EphemeralStorageSize</a></code> | <code>github.com/aws/aws-cdk-go/awscdk/v2.Size</code> | The size of the function’s /tmp directory in MiB. |
| <code><a href="#cdk-constructs.FunctionOptions.property.existingDockerImage">ExistingDockerImage</a></code> | <code>github.com/aws/aws-cdk-go/awscdk/v2.aws_lambda.DockerImageCode</code> | Existing docker image. |
| <code><a href="#cdk-constructs.FunctionOptions.property.filesystem">Filesystem</a></code> | <code>github.com/aws/aws-cdk-go/awscdk/v2.aws_lambda.FileSystem</code> | The filesystem configuration for the lambda function. |
| <code><a href="#cdk-constructs.FunctionOptions.property.legacyEndpoints">LegacyEndpoints</a></code> | <code>*map[string]<a href="#cdk-constructs.LegacyEndpointAlbProps">LegacyEndpointAlbProps</a></code> | Legacy endpoints associated with this lambda. |
| <code><a href="#cdk-constructs.FunctionOptions.property.memorySize">MemorySize</a></code> | <code>*f64</code> | The amount of memory, in MB, that is allocated to your Lambda function. |
| <code><a href="#cdk-constructs.FunctionOptions.property.reservedConcurrentExecutions">ReservedConcurrentExecutions</a></code> | <code>*f64</code> | The maximum of concurrent executions you want to reserve for the function. |
| <code><a href="#cdk-constructs.FunctionOptions.property.timeout">Timeout</a></code> | <code>github.com/aws/aws-cdk-go/awscdk/v2.Duration</code> | The function execution time (in seconds) after which Lambda terminates the function. |

---

##### `ApiGatewayEndpoints`<sup>Optional</sup> <a name="ApiGatewayEndpoints" id="cdk-constructs.FunctionOptions.property.apiGatewayEndpoints"></a>

```go
ApiGatewayEndpoints *map[string]ThronLambdaApiGatewayEndpointProps
```

- *Type:* *map[string]<a href="#cdk-constructs.ThronLambdaApiGatewayEndpointProps">ThronLambdaApiGatewayEndpointProps</a>

Api Gateway endpoints associated with this lambda.

---

##### `Architecture`<sup>Optional</sup> <a name="Architecture" id="cdk-constructs.FunctionOptions.property.architecture"></a>

```go
Architecture Architecture
```

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_lambda.Architecture
- *Default:* lambda.Architecture.X86_64

The architecture the lambda function runs on.

---

##### `AreMultiValueHeadersEnabled`<sup>Optional</sup> <a name="AreMultiValueHeadersEnabled" id="cdk-constructs.FunctionOptions.property.areMultiValueHeadersEnabled"></a>

```go
AreMultiValueHeadersEnabled *bool
```

- *Type:* *bool
- *Default:* false

Whether or not multi value headers are enabled.

If you enable this flag may need to made some slight modification; more info at the following link
https://docs.aws.amazon.com/elasticloadbalancing/latest/application/lambda-functions.html#multi-value-headers

---

##### `Description`<sup>Optional</sup> <a name="Description" id="cdk-constructs.FunctionOptions.property.description"></a>

```go
Description *string
```

- *Type:* *string
- *Default:* No description.

A description of the function.

---

##### `DockerContextPath`<sup>Optional</sup> <a name="DockerContextPath" id="cdk-constructs.FunctionOptions.property.dockerContextPath"></a>

```go
DockerContextPath *string
```

- *Type:* *string

Context of docker build.

---

##### `DockerfileName`<sup>Optional</sup> <a name="DockerfileName" id="cdk-constructs.FunctionOptions.property.dockerfileName"></a>

```go
DockerfileName *string
```

- *Type:* *string
- *Default:* Dockerfile

Name of Dockerfile.

---

##### `Endpoints`<sup>Optional</sup> <a name="Endpoints" id="cdk-constructs.FunctionOptions.property.endpoints"></a>

```go
Endpoints *map[string]ThronEndpointAlbProps
```

- *Type:* *map[string]<a href="#cdk-constructs.ThronEndpointAlbProps">ThronEndpointAlbProps</a>

Endpoints associated with this lambda.

---

##### `Environment`<sup>Optional</sup> <a name="Environment" id="cdk-constructs.FunctionOptions.property.environment"></a>

```go
Environment *map[string]*string
```

- *Type:* *map[string]*string
- *Default:* No environment variables.

Key-value pairs that Lambda caches and makes available for your Lambda functions.

Use environment variables to apply configuration changes, such
as test and production environment configurations, without changing your
Lambda function source code.

---

##### `EphemeralStorageSize`<sup>Optional</sup> <a name="EphemeralStorageSize" id="cdk-constructs.FunctionOptions.property.ephemeralStorageSize"></a>

```go
EphemeralStorageSize Size
```

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.Size
- *Default:* 512 MiB

The size of the function’s /tmp directory in MiB.

---

##### `ExistingDockerImage`<sup>Optional</sup> <a name="ExistingDockerImage" id="cdk-constructs.FunctionOptions.property.existingDockerImage"></a>

```go
ExistingDockerImage DockerImageCode
```

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_lambda.DockerImageCode

Existing docker image.

---

##### `Filesystem`<sup>Optional</sup> <a name="Filesystem" id="cdk-constructs.FunctionOptions.property.filesystem"></a>

```go
Filesystem FileSystem
```

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_lambda.FileSystem
- *Default:* will not mount any filesystem

The filesystem configuration for the lambda function.

---

##### `LegacyEndpoints`<sup>Optional</sup> <a name="LegacyEndpoints" id="cdk-constructs.FunctionOptions.property.legacyEndpoints"></a>

```go
LegacyEndpoints *map[string]LegacyEndpointAlbProps
```

- *Type:* *map[string]<a href="#cdk-constructs.LegacyEndpointAlbProps">LegacyEndpointAlbProps</a>

Legacy endpoints associated with this lambda.

---

##### `MemorySize`<sup>Optional</sup> <a name="MemorySize" id="cdk-constructs.FunctionOptions.property.memorySize"></a>

```go
MemorySize *f64
```

- *Type:* *f64
- *Default:* 128

The amount of memory, in MB, that is allocated to your Lambda function.

Lambda uses this value to proportionally allocate the amount of CPU
power. For more information, see Resource Model in the AWS Lambda
Developer Guide.

---

##### `ReservedConcurrentExecutions`<sup>Optional</sup> <a name="ReservedConcurrentExecutions" id="cdk-constructs.FunctionOptions.property.reservedConcurrentExecutions"></a>

```go
ReservedConcurrentExecutions *f64
```

- *Type:* *f64
- *Default:* No specific limit - account limit.

The maximum of concurrent executions you want to reserve for the function.

---

##### `Timeout`<sup>Optional</sup> <a name="Timeout" id="cdk-constructs.FunctionOptions.property.timeout"></a>

```go
Timeout Duration
```

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.Duration
- *Default:* Duration.seconds(3)

The function execution time (in seconds) after which Lambda terminates the function.

Because the execution time affects cost, set this value
based on the function's expected execution time.

---

### LambdaConf <a name="LambdaConf" id="cdk-constructs.LambdaConf"></a>

#### Initializer <a name="Initializer" id="cdk-constructs.LambdaConf.Initializer"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

&cdkconstructs.LambdaConf {
	ComputeType: github.com/aws/aws-cdk-go/awscdk/v2.aws_codebuild.ComputeType,
	CustomBuildImage: github.com/aws/aws-cdk-go/awscdk/v2.aws_codebuild.IBuildImage,
	EnvironmentalVariables: *map[string]github.com/aws/aws-cdk-go/awscdk/v2.aws_codebuild.BuildEnvironmentVariable,
	DestinationEcrRepository: github.com/aws/aws-cdk-go/awscdk/v2.aws_ecr.Repository,
}
```

#### Properties <a name="Properties" id="Properties"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.LambdaConf.property.computeType">ComputeType</a></code> | <code>github.com/aws/aws-cdk-go/awscdk/v2.aws_codebuild.ComputeType</code> | Specify the size of the build containers. See https://docs.aws.amazon.com/codebuild/latest/userguide/build-env-ref-compute-types.html#environment.types for reference. |
| <code><a href="#cdk-constructs.LambdaConf.property.customBuildImage">CustomBuildImage</a></code> | <code>github.com/aws/aws-cdk-go/awscdk/v2.aws_codebuild.IBuildImage</code> | Build image to be used fot this step. |
| <code><a href="#cdk-constructs.LambdaConf.property.environmentalVariables">EnvironmentalVariables</a></code> | <code>*map[string]github.com/aws/aws-cdk-go/awscdk/v2.aws_codebuild.BuildEnvironmentVariable</code> | Map of additional env vars to pass to the build container. |
| <code><a href="#cdk-constructs.LambdaConf.property.destinationEcrRepository">DestinationEcrRepository</a></code> | <code>github.com/aws/aws-cdk-go/awscdk/v2.aws_ecr.Repository</code> | *No description.* |

---

##### `ComputeType`<sup>Optional</sup> <a name="ComputeType" id="cdk-constructs.LambdaConf.property.computeType"></a>

```go
ComputeType ComputeType
```

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_codebuild.ComputeType

Specify the size of the build containers. See https://docs.aws.amazon.com/codebuild/latest/userguide/build-env-ref-compute-types.html#environment.types for reference.

Defaults to `ComputeType.SMALL`

---

##### `CustomBuildImage`<sup>Optional</sup> <a name="CustomBuildImage" id="cdk-constructs.LambdaConf.property.customBuildImage"></a>

```go
CustomBuildImage IBuildImage
```

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_codebuild.IBuildImage

Build image to be used fot this step.

---

##### `EnvironmentalVariables`<sup>Optional</sup> <a name="EnvironmentalVariables" id="cdk-constructs.LambdaConf.property.environmentalVariables"></a>

```go
EnvironmentalVariables *map[string]BuildEnvironmentVariable
```

- *Type:* *map[string]github.com/aws/aws-cdk-go/awscdk/v2.aws_codebuild.BuildEnvironmentVariable

Map of additional env vars to pass to the build container.

---

##### `DestinationEcrRepository`<sup>Required</sup> <a name="DestinationEcrRepository" id="cdk-constructs.LambdaConf.property.destinationEcrRepository"></a>

```go
DestinationEcrRepository Repository
```

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_ecr.Repository

---

### LegacyEndpointAlbProps <a name="LegacyEndpointAlbProps" id="cdk-constructs.LegacyEndpointAlbProps"></a>

#### Initializer <a name="Initializer" id="cdk-constructs.LegacyEndpointAlbProps.Initializer"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

&cdkconstructs.LegacyEndpointAlbProps {
	RoutingTokenPrefix: *string,
	ServiceGroup: git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs.ServiceGroup,
	DeleteExistingDns: *bool,
	Stack: github.com/aws/aws-cdk-go/awscdk/v2.Stack,
}
```

#### Properties <a name="Properties" id="Properties"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.LegacyEndpointAlbProps.property.routingTokenPrefix">RoutingTokenPrefix</a></code> | <code>*string</code> | Routing path for the service, validated against `serviceGroup`. |
| <code><a href="#cdk-constructs.LegacyEndpointAlbProps.property.serviceGroup">ServiceGroup</a></code> | <code><a href="#cdk-constructs.ServiceGroup">ServiceGroup</a></code> | Service group of the service. |
| <code><a href="#cdk-constructs.LegacyEndpointAlbProps.property.deleteExistingDns">DeleteExistingDns</a></code> | <code>*bool</code> | DANGEROUS: Overwrite dns record if it already exists, otherwise it creates it. |
| <code><a href="#cdk-constructs.LegacyEndpointAlbProps.property.stack">Stack</a></code> | <code>github.com/aws/aws-cdk-go/awscdk/v2.Stack</code> | The reference of parent Stack. |

---

##### `RoutingTokenPrefix`<sup>Required</sup> <a name="RoutingTokenPrefix" id="cdk-constructs.LegacyEndpointAlbProps.property.routingTokenPrefix"></a>

```go
RoutingTokenPrefix *string
```

- *Type:* *string

Routing path for the service, validated against `serviceGroup`.

---

##### `ServiceGroup`<sup>Required</sup> <a name="ServiceGroup" id="cdk-constructs.LegacyEndpointAlbProps.property.serviceGroup"></a>

```go
ServiceGroup ServiceGroup
```

- *Type:* <a href="#cdk-constructs.ServiceGroup">ServiceGroup</a>

Service group of the service.

---

##### `DeleteExistingDns`<sup>Optional</sup> <a name="DeleteExistingDns" id="cdk-constructs.LegacyEndpointAlbProps.property.deleteExistingDns"></a>

```go
DeleteExistingDns *bool
```

- *Type:* *bool
- *Default:* false

DANGEROUS: Overwrite dns record if it already exists, otherwise it creates it.

---

##### `Stack`<sup>Optional</sup> <a name="Stack" id="cdk-constructs.LegacyEndpointAlbProps.property.stack"></a>

```go
Stack Stack
```

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.Stack

The reference of parent Stack.

---

### NewRelicFunctionOptions <a name="NewRelicFunctionOptions" id="cdk-constructs.NewRelicFunctionOptions"></a>

#### Initializer <a name="Initializer" id="cdk-constructs.NewRelicFunctionOptions.Initializer"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

&cdkconstructs.NewRelicFunctionOptions {
	ApiGatewayEndpoints: *map[string]git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs.ThronLambdaApiGatewayEndpointProps,
	Architecture: github.com/aws/aws-cdk-go/awscdk/v2.aws_lambda.Architecture,
	AreMultiValueHeadersEnabled: *bool,
	Description: *string,
	DockerContextPath: *string,
	DockerfileName: *string,
	Endpoints: *map[string]git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs.ThronEndpointAlbProps,
	Environment: *map[string]*string,
	EphemeralStorageSize: github.com/aws/aws-cdk-go/awscdk/v2.Size,
	ExistingDockerImage: github.com/aws/aws-cdk-go/awscdk/v2.aws_lambda.DockerImageCode,
	Filesystem: github.com/aws/aws-cdk-go/awscdk/v2.aws_lambda.FileSystem,
	LegacyEndpoints: *map[string]git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs.LegacyEndpointAlbProps,
	MemorySize: *f64,
	ReservedConcurrentExecutions: *f64,
	Timeout: github.com/aws/aws-cdk-go/awscdk/v2.Duration,
	NewRelicConfigOverrides: git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs.NewRelicLambdaConfigOverrides,
}
```

#### Properties <a name="Properties" id="Properties"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.NewRelicFunctionOptions.property.apiGatewayEndpoints">ApiGatewayEndpoints</a></code> | <code>*map[string]<a href="#cdk-constructs.ThronLambdaApiGatewayEndpointProps">ThronLambdaApiGatewayEndpointProps</a></code> | Api Gateway endpoints associated with this lambda. |
| <code><a href="#cdk-constructs.NewRelicFunctionOptions.property.architecture">Architecture</a></code> | <code>github.com/aws/aws-cdk-go/awscdk/v2.aws_lambda.Architecture</code> | The architecture the lambda function runs on. |
| <code><a href="#cdk-constructs.NewRelicFunctionOptions.property.areMultiValueHeadersEnabled">AreMultiValueHeadersEnabled</a></code> | <code>*bool</code> | Whether or not multi value headers are enabled. |
| <code><a href="#cdk-constructs.NewRelicFunctionOptions.property.description">Description</a></code> | <code>*string</code> | A description of the function. |
| <code><a href="#cdk-constructs.NewRelicFunctionOptions.property.dockerContextPath">DockerContextPath</a></code> | <code>*string</code> | Context of docker build. |
| <code><a href="#cdk-constructs.NewRelicFunctionOptions.property.dockerfileName">DockerfileName</a></code> | <code>*string</code> | Name of Dockerfile. |
| <code><a href="#cdk-constructs.NewRelicFunctionOptions.property.endpoints">Endpoints</a></code> | <code>*map[string]<a href="#cdk-constructs.ThronEndpointAlbProps">ThronEndpointAlbProps</a></code> | Endpoints associated with this lambda. |
| <code><a href="#cdk-constructs.NewRelicFunctionOptions.property.environment">Environment</a></code> | <code>*map[string]*string</code> | Key-value pairs that Lambda caches and makes available for your Lambda functions. |
| <code><a href="#cdk-constructs.NewRelicFunctionOptions.property.ephemeralStorageSize">EphemeralStorageSize</a></code> | <code>github.com/aws/aws-cdk-go/awscdk/v2.Size</code> | The size of the function’s /tmp directory in MiB. |
| <code><a href="#cdk-constructs.NewRelicFunctionOptions.property.existingDockerImage">ExistingDockerImage</a></code> | <code>github.com/aws/aws-cdk-go/awscdk/v2.aws_lambda.DockerImageCode</code> | Existing docker image. |
| <code><a href="#cdk-constructs.NewRelicFunctionOptions.property.filesystem">Filesystem</a></code> | <code>github.com/aws/aws-cdk-go/awscdk/v2.aws_lambda.FileSystem</code> | The filesystem configuration for the lambda function. |
| <code><a href="#cdk-constructs.NewRelicFunctionOptions.property.legacyEndpoints">LegacyEndpoints</a></code> | <code>*map[string]<a href="#cdk-constructs.LegacyEndpointAlbProps">LegacyEndpointAlbProps</a></code> | Legacy endpoints associated with this lambda. |
| <code><a href="#cdk-constructs.NewRelicFunctionOptions.property.memorySize">MemorySize</a></code> | <code>*f64</code> | The amount of memory, in MB, that is allocated to your Lambda function. |
| <code><a href="#cdk-constructs.NewRelicFunctionOptions.property.reservedConcurrentExecutions">ReservedConcurrentExecutions</a></code> | <code>*f64</code> | The maximum of concurrent executions you want to reserve for the function. |
| <code><a href="#cdk-constructs.NewRelicFunctionOptions.property.timeout">Timeout</a></code> | <code>github.com/aws/aws-cdk-go/awscdk/v2.Duration</code> | The function execution time (in seconds) after which Lambda terminates the function. |
| <code><a href="#cdk-constructs.NewRelicFunctionOptions.property.newRelicConfigOverrides">NewRelicConfigOverrides</a></code> | <code><a href="#cdk-constructs.NewRelicLambdaConfigOverrides">NewRelicLambdaConfigOverrides</a></code> | Explicit Overrides for NewRelic Configuration. |

---

##### `ApiGatewayEndpoints`<sup>Optional</sup> <a name="ApiGatewayEndpoints" id="cdk-constructs.NewRelicFunctionOptions.property.apiGatewayEndpoints"></a>

```go
ApiGatewayEndpoints *map[string]ThronLambdaApiGatewayEndpointProps
```

- *Type:* *map[string]<a href="#cdk-constructs.ThronLambdaApiGatewayEndpointProps">ThronLambdaApiGatewayEndpointProps</a>

Api Gateway endpoints associated with this lambda.

---

##### `Architecture`<sup>Optional</sup> <a name="Architecture" id="cdk-constructs.NewRelicFunctionOptions.property.architecture"></a>

```go
Architecture Architecture
```

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_lambda.Architecture
- *Default:* lambda.Architecture.X86_64

The architecture the lambda function runs on.

---

##### `AreMultiValueHeadersEnabled`<sup>Optional</sup> <a name="AreMultiValueHeadersEnabled" id="cdk-constructs.NewRelicFunctionOptions.property.areMultiValueHeadersEnabled"></a>

```go
AreMultiValueHeadersEnabled *bool
```

- *Type:* *bool
- *Default:* false

Whether or not multi value headers are enabled.

If you enable this flag may need to made some slight modification; more info at the following link
https://docs.aws.amazon.com/elasticloadbalancing/latest/application/lambda-functions.html#multi-value-headers

---

##### `Description`<sup>Optional</sup> <a name="Description" id="cdk-constructs.NewRelicFunctionOptions.property.description"></a>

```go
Description *string
```

- *Type:* *string
- *Default:* No description.

A description of the function.

---

##### `DockerContextPath`<sup>Optional</sup> <a name="DockerContextPath" id="cdk-constructs.NewRelicFunctionOptions.property.dockerContextPath"></a>

```go
DockerContextPath *string
```

- *Type:* *string

Context of docker build.

---

##### `DockerfileName`<sup>Optional</sup> <a name="DockerfileName" id="cdk-constructs.NewRelicFunctionOptions.property.dockerfileName"></a>

```go
DockerfileName *string
```

- *Type:* *string
- *Default:* Dockerfile

Name of Dockerfile.

---

##### `Endpoints`<sup>Optional</sup> <a name="Endpoints" id="cdk-constructs.NewRelicFunctionOptions.property.endpoints"></a>

```go
Endpoints *map[string]ThronEndpointAlbProps
```

- *Type:* *map[string]<a href="#cdk-constructs.ThronEndpointAlbProps">ThronEndpointAlbProps</a>

Endpoints associated with this lambda.

---

##### `Environment`<sup>Optional</sup> <a name="Environment" id="cdk-constructs.NewRelicFunctionOptions.property.environment"></a>

```go
Environment *map[string]*string
```

- *Type:* *map[string]*string
- *Default:* No environment variables.

Key-value pairs that Lambda caches and makes available for your Lambda functions.

Use environment variables to apply configuration changes, such
as test and production environment configurations, without changing your
Lambda function source code.

---

##### `EphemeralStorageSize`<sup>Optional</sup> <a name="EphemeralStorageSize" id="cdk-constructs.NewRelicFunctionOptions.property.ephemeralStorageSize"></a>

```go
EphemeralStorageSize Size
```

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.Size
- *Default:* 512 MiB

The size of the function’s /tmp directory in MiB.

---

##### `ExistingDockerImage`<sup>Optional</sup> <a name="ExistingDockerImage" id="cdk-constructs.NewRelicFunctionOptions.property.existingDockerImage"></a>

```go
ExistingDockerImage DockerImageCode
```

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_lambda.DockerImageCode

Existing docker image.

---

##### `Filesystem`<sup>Optional</sup> <a name="Filesystem" id="cdk-constructs.NewRelicFunctionOptions.property.filesystem"></a>

```go
Filesystem FileSystem
```

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_lambda.FileSystem
- *Default:* will not mount any filesystem

The filesystem configuration for the lambda function.

---

##### `LegacyEndpoints`<sup>Optional</sup> <a name="LegacyEndpoints" id="cdk-constructs.NewRelicFunctionOptions.property.legacyEndpoints"></a>

```go
LegacyEndpoints *map[string]LegacyEndpointAlbProps
```

- *Type:* *map[string]<a href="#cdk-constructs.LegacyEndpointAlbProps">LegacyEndpointAlbProps</a>

Legacy endpoints associated with this lambda.

---

##### `MemorySize`<sup>Optional</sup> <a name="MemorySize" id="cdk-constructs.NewRelicFunctionOptions.property.memorySize"></a>

```go
MemorySize *f64
```

- *Type:* *f64
- *Default:* 128

The amount of memory, in MB, that is allocated to your Lambda function.

Lambda uses this value to proportionally allocate the amount of CPU
power. For more information, see Resource Model in the AWS Lambda
Developer Guide.

---

##### `ReservedConcurrentExecutions`<sup>Optional</sup> <a name="ReservedConcurrentExecutions" id="cdk-constructs.NewRelicFunctionOptions.property.reservedConcurrentExecutions"></a>

```go
ReservedConcurrentExecutions *f64
```

- *Type:* *f64
- *Default:* No specific limit - account limit.

The maximum of concurrent executions you want to reserve for the function.

---

##### `Timeout`<sup>Optional</sup> <a name="Timeout" id="cdk-constructs.NewRelicFunctionOptions.property.timeout"></a>

```go
Timeout Duration
```

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.Duration
- *Default:* Duration.seconds(3)

The function execution time (in seconds) after which Lambda terminates the function.

Because the execution time affects cost, set this value
based on the function's expected execution time.

---

##### `NewRelicConfigOverrides`<sup>Optional</sup> <a name="NewRelicConfigOverrides" id="cdk-constructs.NewRelicFunctionOptions.property.newRelicConfigOverrides"></a>

```go
NewRelicConfigOverrides NewRelicLambdaConfigOverrides
```

- *Type:* <a href="#cdk-constructs.NewRelicLambdaConfigOverrides">NewRelicLambdaConfigOverrides</a>
- *Default:* Empty object with no overrides

Explicit Overrides for NewRelic Configuration.

---

### NewRelicLambdaConfig <a name="NewRelicLambdaConfig" id="cdk-constructs.NewRelicLambdaConfig"></a>

#### Initializer <a name="Initializer" id="cdk-constructs.NewRelicLambdaConfig.Initializer"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

&cdkconstructs.NewRelicLambdaConfig {
	NewRelicAccountId: *string,
	NewRelicDistributedTracingEnabled: *bool,
	NewRelicExtensionLogsEnabled: *bool,
	NewRelicExtensionSendFunctionLogs: *bool,
	NewRelicIgnoreExtensionChecks: *[]git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs.NewRelicIgnoreExtensionChecksOption,
	NewRelicLambdaExtensionEnabled: *bool,
	NewRelicLicenseKey: *string,
	NewRelicLicenseKeyParameterName: *string,
	NewRelicTrustedAccountKey: *string,
}
```

#### Properties <a name="Properties" id="Properties"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.NewRelicLambdaConfig.property.newRelicAccountId">NewRelicAccountId</a></code> | <code>*string</code> | *No description.* |
| <code><a href="#cdk-constructs.NewRelicLambdaConfig.property.newRelicDistributedTracingEnabled">NewRelicDistributedTracingEnabled</a></code> | <code>*bool</code> | *No description.* |
| <code><a href="#cdk-constructs.NewRelicLambdaConfig.property.newRelicExtensionLogsEnabled">NewRelicExtensionLogsEnabled</a></code> | <code>*bool</code> | *No description.* |
| <code><a href="#cdk-constructs.NewRelicLambdaConfig.property.newRelicExtensionSendFunctionLogs">NewRelicExtensionSendFunctionLogs</a></code> | <code>*bool</code> | *No description.* |
| <code><a href="#cdk-constructs.NewRelicLambdaConfig.property.newRelicIgnoreExtensionChecks">NewRelicIgnoreExtensionChecks</a></code> | <code>*[]<a href="#cdk-constructs.NewRelicIgnoreExtensionChecksOption">NewRelicIgnoreExtensionChecksOption</a></code> | *No description.* |
| <code><a href="#cdk-constructs.NewRelicLambdaConfig.property.newRelicLambdaExtensionEnabled">NewRelicLambdaExtensionEnabled</a></code> | <code>*bool</code> | *No description.* |
| <code><a href="#cdk-constructs.NewRelicLambdaConfig.property.newRelicLicenseKey">NewRelicLicenseKey</a></code> | <code>*string</code> | *No description.* |
| <code><a href="#cdk-constructs.NewRelicLambdaConfig.property.newRelicLicenseKeyParameterName">NewRelicLicenseKeyParameterName</a></code> | <code>*string</code> | *No description.* |
| <code><a href="#cdk-constructs.NewRelicLambdaConfig.property.newRelicTrustedAccountKey">NewRelicTrustedAccountKey</a></code> | <code>*string</code> | *No description.* |

---

##### `NewRelicAccountId`<sup>Required</sup> <a name="NewRelicAccountId" id="cdk-constructs.NewRelicLambdaConfig.property.newRelicAccountId"></a>

```go
NewRelicAccountId *string
```

- *Type:* *string

---

##### `NewRelicDistributedTracingEnabled`<sup>Required</sup> <a name="NewRelicDistributedTracingEnabled" id="cdk-constructs.NewRelicLambdaConfig.property.newRelicDistributedTracingEnabled"></a>

```go
NewRelicDistributedTracingEnabled *bool
```

- *Type:* *bool

---

##### `NewRelicExtensionLogsEnabled`<sup>Required</sup> <a name="NewRelicExtensionLogsEnabled" id="cdk-constructs.NewRelicLambdaConfig.property.newRelicExtensionLogsEnabled"></a>

```go
NewRelicExtensionLogsEnabled *bool
```

- *Type:* *bool

---

##### `NewRelicExtensionSendFunctionLogs`<sup>Required</sup> <a name="NewRelicExtensionSendFunctionLogs" id="cdk-constructs.NewRelicLambdaConfig.property.newRelicExtensionSendFunctionLogs"></a>

```go
NewRelicExtensionSendFunctionLogs *bool
```

- *Type:* *bool

---

##### `NewRelicIgnoreExtensionChecks`<sup>Required</sup> <a name="NewRelicIgnoreExtensionChecks" id="cdk-constructs.NewRelicLambdaConfig.property.newRelicIgnoreExtensionChecks"></a>

```go
NewRelicIgnoreExtensionChecks *[]NewRelicIgnoreExtensionChecksOption
```

- *Type:* *[]<a href="#cdk-constructs.NewRelicIgnoreExtensionChecksOption">NewRelicIgnoreExtensionChecksOption</a>

---

##### `NewRelicLambdaExtensionEnabled`<sup>Required</sup> <a name="NewRelicLambdaExtensionEnabled" id="cdk-constructs.NewRelicLambdaConfig.property.newRelicLambdaExtensionEnabled"></a>

```go
NewRelicLambdaExtensionEnabled *bool
```

- *Type:* *bool

---

##### `NewRelicLicenseKey`<sup>Required</sup> <a name="NewRelicLicenseKey" id="cdk-constructs.NewRelicLambdaConfig.property.newRelicLicenseKey"></a>

```go
NewRelicLicenseKey *string
```

- *Type:* *string

---

##### `NewRelicLicenseKeyParameterName`<sup>Required</sup> <a name="NewRelicLicenseKeyParameterName" id="cdk-constructs.NewRelicLambdaConfig.property.newRelicLicenseKeyParameterName"></a>

```go
NewRelicLicenseKeyParameterName *string
```

- *Type:* *string

---

##### `NewRelicTrustedAccountKey`<sup>Required</sup> <a name="NewRelicTrustedAccountKey" id="cdk-constructs.NewRelicLambdaConfig.property.newRelicTrustedAccountKey"></a>

```go
NewRelicTrustedAccountKey *string
```

- *Type:* *string

---

### NewRelicLambdaConfigOverrides <a name="NewRelicLambdaConfigOverrides" id="cdk-constructs.NewRelicLambdaConfigOverrides"></a>

#### Initializer <a name="Initializer" id="cdk-constructs.NewRelicLambdaConfigOverrides.Initializer"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

&cdkconstructs.NewRelicLambdaConfigOverrides {
	NewRelicAccountId: *string,
	NewRelicDistributedTracingEnabled: *bool,
	NewRelicExtensionLogsEnabled: *bool,
	NewRelicExtensionSendFunctionLogs: *bool,
	NewRelicIgnoreExtensionChecks: *[]git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs.NewRelicIgnoreExtensionChecksOption,
	NewRelicLambdaExtensionEnabled: *bool,
	NewRelicLicenseKey: *string,
	NewRelicLicenseKeyParameterName: *string,
	NewRelicTrustedAccountKey: *string,
}
```

#### Properties <a name="Properties" id="Properties"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.NewRelicLambdaConfigOverrides.property.newRelicAccountId">NewRelicAccountId</a></code> | <code>*string</code> | *No description.* |
| <code><a href="#cdk-constructs.NewRelicLambdaConfigOverrides.property.newRelicDistributedTracingEnabled">NewRelicDistributedTracingEnabled</a></code> | <code>*bool</code> | *No description.* |
| <code><a href="#cdk-constructs.NewRelicLambdaConfigOverrides.property.newRelicExtensionLogsEnabled">NewRelicExtensionLogsEnabled</a></code> | <code>*bool</code> | *No description.* |
| <code><a href="#cdk-constructs.NewRelicLambdaConfigOverrides.property.newRelicExtensionSendFunctionLogs">NewRelicExtensionSendFunctionLogs</a></code> | <code>*bool</code> | *No description.* |
| <code><a href="#cdk-constructs.NewRelicLambdaConfigOverrides.property.newRelicIgnoreExtensionChecks">NewRelicIgnoreExtensionChecks</a></code> | <code>*[]<a href="#cdk-constructs.NewRelicIgnoreExtensionChecksOption">NewRelicIgnoreExtensionChecksOption</a></code> | *No description.* |
| <code><a href="#cdk-constructs.NewRelicLambdaConfigOverrides.property.newRelicLambdaExtensionEnabled">NewRelicLambdaExtensionEnabled</a></code> | <code>*bool</code> | *No description.* |
| <code><a href="#cdk-constructs.NewRelicLambdaConfigOverrides.property.newRelicLicenseKey">NewRelicLicenseKey</a></code> | <code>*string</code> | *No description.* |
| <code><a href="#cdk-constructs.NewRelicLambdaConfigOverrides.property.newRelicLicenseKeyParameterName">NewRelicLicenseKeyParameterName</a></code> | <code>*string</code> | *No description.* |
| <code><a href="#cdk-constructs.NewRelicLambdaConfigOverrides.property.newRelicTrustedAccountKey">NewRelicTrustedAccountKey</a></code> | <code>*string</code> | *No description.* |

---

##### `NewRelicAccountId`<sup>Optional</sup> <a name="NewRelicAccountId" id="cdk-constructs.NewRelicLambdaConfigOverrides.property.newRelicAccountId"></a>

```go
NewRelicAccountId *string
```

- *Type:* *string

---

##### `NewRelicDistributedTracingEnabled`<sup>Optional</sup> <a name="NewRelicDistributedTracingEnabled" id="cdk-constructs.NewRelicLambdaConfigOverrides.property.newRelicDistributedTracingEnabled"></a>

```go
NewRelicDistributedTracingEnabled *bool
```

- *Type:* *bool

---

##### `NewRelicExtensionLogsEnabled`<sup>Optional</sup> <a name="NewRelicExtensionLogsEnabled" id="cdk-constructs.NewRelicLambdaConfigOverrides.property.newRelicExtensionLogsEnabled"></a>

```go
NewRelicExtensionLogsEnabled *bool
```

- *Type:* *bool

---

##### `NewRelicExtensionSendFunctionLogs`<sup>Optional</sup> <a name="NewRelicExtensionSendFunctionLogs" id="cdk-constructs.NewRelicLambdaConfigOverrides.property.newRelicExtensionSendFunctionLogs"></a>

```go
NewRelicExtensionSendFunctionLogs *bool
```

- *Type:* *bool

---

##### `NewRelicIgnoreExtensionChecks`<sup>Optional</sup> <a name="NewRelicIgnoreExtensionChecks" id="cdk-constructs.NewRelicLambdaConfigOverrides.property.newRelicIgnoreExtensionChecks"></a>

```go
NewRelicIgnoreExtensionChecks *[]NewRelicIgnoreExtensionChecksOption
```

- *Type:* *[]<a href="#cdk-constructs.NewRelicIgnoreExtensionChecksOption">NewRelicIgnoreExtensionChecksOption</a>

---

##### `NewRelicLambdaExtensionEnabled`<sup>Optional</sup> <a name="NewRelicLambdaExtensionEnabled" id="cdk-constructs.NewRelicLambdaConfigOverrides.property.newRelicLambdaExtensionEnabled"></a>

```go
NewRelicLambdaExtensionEnabled *bool
```

- *Type:* *bool

---

##### `NewRelicLicenseKey`<sup>Optional</sup> <a name="NewRelicLicenseKey" id="cdk-constructs.NewRelicLambdaConfigOverrides.property.newRelicLicenseKey"></a>

```go
NewRelicLicenseKey *string
```

- *Type:* *string

---

##### `NewRelicLicenseKeyParameterName`<sup>Optional</sup> <a name="NewRelicLicenseKeyParameterName" id="cdk-constructs.NewRelicLambdaConfigOverrides.property.newRelicLicenseKeyParameterName"></a>

```go
NewRelicLicenseKeyParameterName *string
```

- *Type:* *string

---

##### `NewRelicTrustedAccountKey`<sup>Optional</sup> <a name="NewRelicTrustedAccountKey" id="cdk-constructs.NewRelicLambdaConfigOverrides.property.newRelicTrustedAccountKey"></a>

```go
NewRelicTrustedAccountKey *string
```

- *Type:* *string

---

### NotifyConf <a name="NotifyConf" id="cdk-constructs.NotifyConf"></a>

Configuration for the notifier webhook.

#### Initializer <a name="Initializer" id="cdk-constructs.NotifyConf.Initializer"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

&cdkconstructs.NotifyConf {
	NotifyCapabilities: *[]git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs.PipelineCapability,
	WebhookUrl: *string,
}
```

#### Properties <a name="Properties" id="Properties"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.NotifyConf.property.notifyCapabilities">NotifyCapabilities</a></code> | <code>*[]<a href="#cdk-constructs.PipelineCapability">PipelineCapability</a></code> | List of capabilities for notification purposes. |
| <code><a href="#cdk-constructs.NotifyConf.property.webhookUrl">WebhookUrl</a></code> | <code>*string</code> | Ms Teams webhook url to send the notifications to. |

---

##### `NotifyCapabilities`<sup>Required</sup> <a name="NotifyCapabilities" id="cdk-constructs.NotifyConf.property.notifyCapabilities"></a>

```go
NotifyCapabilities *[]PipelineCapability
```

- *Type:* *[]<a href="#cdk-constructs.PipelineCapability">PipelineCapability</a>

List of capabilities for notification purposes.

All of them must start with `NOTIFY_ON`

---

##### `WebhookUrl`<sup>Required</sup> <a name="WebhookUrl" id="cdk-constructs.NotifyConf.property.webhookUrl"></a>

```go
WebhookUrl *string
```

- *Type:* *string

Ms Teams webhook url to send the notifications to.

---

### NotifyLambdaEnv <a name="NotifyLambdaEnv" id="cdk-constructs.NotifyLambdaEnv"></a>

#### Initializer <a name="Initializer" id="cdk-constructs.NotifyLambdaEnv.Initializer"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

&cdkconstructs.NotifyLambdaEnv {
	Branch: *string,
	Env: *string,
	ProjectId: *string,
	Repository: *string,
	WebhookUrl: *string,
}
```

#### Properties <a name="Properties" id="Properties"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.NotifyLambdaEnv.property.branch">Branch</a></code> | <code>*string</code> | *No description.* |
| <code><a href="#cdk-constructs.NotifyLambdaEnv.property.env">Env</a></code> | <code>*string</code> | *No description.* |
| <code><a href="#cdk-constructs.NotifyLambdaEnv.property.projectId">ProjectId</a></code> | <code>*string</code> | *No description.* |
| <code><a href="#cdk-constructs.NotifyLambdaEnv.property.repository">Repository</a></code> | <code>*string</code> | *No description.* |
| <code><a href="#cdk-constructs.NotifyLambdaEnv.property.webhookUrl">WebhookUrl</a></code> | <code>*string</code> | *No description.* |

---

##### `Branch`<sup>Required</sup> <a name="Branch" id="cdk-constructs.NotifyLambdaEnv.property.branch"></a>

```go
Branch *string
```

- *Type:* *string

---

##### `Env`<sup>Required</sup> <a name="Env" id="cdk-constructs.NotifyLambdaEnv.property.env"></a>

```go
Env *string
```

- *Type:* *string

---

##### `ProjectId`<sup>Required</sup> <a name="ProjectId" id="cdk-constructs.NotifyLambdaEnv.property.projectId"></a>

```go
ProjectId *string
```

- *Type:* *string

---

##### `Repository`<sup>Required</sup> <a name="Repository" id="cdk-constructs.NotifyLambdaEnv.property.repository"></a>

```go
Repository *string
```

- *Type:* *string

---

##### `WebhookUrl`<sup>Required</sup> <a name="WebhookUrl" id="cdk-constructs.NotifyLambdaEnv.property.webhookUrl"></a>

```go
WebhookUrl *string
```

- *Type:* *string

---

### OptionalServiceProps <a name="OptionalServiceProps" id="cdk-constructs.OptionalServiceProps"></a>

#### Initializer <a name="Initializer" id="cdk-constructs.OptionalServiceProps.Initializer"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

&cdkconstructs.OptionalServiceProps {
	ServiceGroup: git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs.ServiceGroup,
	Version: *f64,
	Visibility: git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs.EndpointVisibility,
}
```

#### Properties <a name="Properties" id="Properties"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.OptionalServiceProps.property.serviceGroup">ServiceGroup</a></code> | <code><a href="#cdk-constructs.ServiceGroup">ServiceGroup</a></code> | Service group of the service. |
| <code><a href="#cdk-constructs.OptionalServiceProps.property.version">Version</a></code> | <code>*f64</code> | The version of the API exposed by the endpoint. |
| <code><a href="#cdk-constructs.OptionalServiceProps.property.visibility">Visibility</a></code> | <code><a href="#cdk-constructs.EndpointVisibility">EndpointVisibility</a></code> | Wether the endpoint is private or public. |

---

##### `ServiceGroup`<sup>Required</sup> <a name="ServiceGroup" id="cdk-constructs.OptionalServiceProps.property.serviceGroup"></a>

```go
ServiceGroup ServiceGroup
```

- *Type:* <a href="#cdk-constructs.ServiceGroup">ServiceGroup</a>
- *Default:* ServiceGroup.VIEW

Service group of the service.

---

##### `Version`<sup>Required</sup> <a name="Version" id="cdk-constructs.OptionalServiceProps.property.version"></a>

```go
Version *f64
```

- *Type:* *f64
- *Default:* 1

The version of the API exposed by the endpoint.

---

##### `Visibility`<sup>Required</sup> <a name="Visibility" id="cdk-constructs.OptionalServiceProps.property.visibility"></a>

```go
Visibility EndpointVisibility
```

- *Type:* <a href="#cdk-constructs.EndpointVisibility">EndpointVisibility</a>
- *Default:* EndpointVisibility.PRIVATE

Wether the endpoint is private or public.

---

### OptionalServicePropsPartial <a name="OptionalServicePropsPartial" id="cdk-constructs.OptionalServicePropsPartial"></a>

#### Initializer <a name="Initializer" id="cdk-constructs.OptionalServicePropsPartial.Initializer"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

&cdkconstructs.OptionalServicePropsPartial {
	ServiceGroup: git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs.ServiceGroup,
	Version: *f64,
	Visibility: git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs.EndpointVisibility,
}
```

#### Properties <a name="Properties" id="Properties"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.OptionalServicePropsPartial.property.serviceGroup">ServiceGroup</a></code> | <code><a href="#cdk-constructs.ServiceGroup">ServiceGroup</a></code> | Service group of the service. |
| <code><a href="#cdk-constructs.OptionalServicePropsPartial.property.version">Version</a></code> | <code>*f64</code> | The version of the API exposed by the endpoint. |
| <code><a href="#cdk-constructs.OptionalServicePropsPartial.property.visibility">Visibility</a></code> | <code><a href="#cdk-constructs.EndpointVisibility">EndpointVisibility</a></code> | Wether the endpoint is private or public. |

---

##### `ServiceGroup`<sup>Optional</sup> <a name="ServiceGroup" id="cdk-constructs.OptionalServicePropsPartial.property.serviceGroup"></a>

```go
ServiceGroup ServiceGroup
```

- *Type:* <a href="#cdk-constructs.ServiceGroup">ServiceGroup</a>
- *Default:* ServiceGroup.VIEW

Service group of the service.

---

##### `Version`<sup>Optional</sup> <a name="Version" id="cdk-constructs.OptionalServicePropsPartial.property.version"></a>

```go
Version *f64
```

- *Type:* *f64
- *Default:* 1

The version of the API exposed by the endpoint.

---

##### `Visibility`<sup>Optional</sup> <a name="Visibility" id="cdk-constructs.OptionalServicePropsPartial.property.visibility"></a>

```go
Visibility EndpointVisibility
```

- *Type:* <a href="#cdk-constructs.EndpointVisibility">EndpointVisibility</a>
- *Default:* EndpointVisibility.PRIVATE

Wether the endpoint is private or public.

---

### OtherAccountPeeringConfig <a name="OtherAccountPeeringConfig" id="cdk-constructs.OtherAccountPeeringConfig"></a>

#### Initializer <a name="Initializer" id="cdk-constructs.OtherAccountPeeringConfig.Initializer"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

&cdkconstructs.OtherAccountPeeringConfig {
	OtherVpcAccountId: *string,
	OtherVpcCidr: *string,
	OtherVpcId: *string,
	OtherVpcRegion: *string,
	UniquePeeringId: *string,
}
```

#### Properties <a name="Properties" id="Properties"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.OtherAccountPeeringConfig.property.otherVpcAccountId">OtherVpcAccountId</a></code> | <code>*string</code> | VPC to be peered account's ID. |
| <code><a href="#cdk-constructs.OtherAccountPeeringConfig.property.otherVpcCidr">OtherVpcCidr</a></code> | <code>*string</code> | VPC to be peered mnemonic Id. |
| <code><a href="#cdk-constructs.OtherAccountPeeringConfig.property.otherVpcId">OtherVpcId</a></code> | <code>*string</code> | VPC to be peered vpcId. |
| <code><a href="#cdk-constructs.OtherAccountPeeringConfig.property.otherVpcRegion">OtherVpcRegion</a></code> | <code>*string</code> | VPC to be peered region. |
| <code><a href="#cdk-constructs.OtherAccountPeeringConfig.property.uniquePeeringId">UniquePeeringId</a></code> | <code>*string</code> | VPC to be peered mnemonic Id. |

---

##### `OtherVpcAccountId`<sup>Required</sup> <a name="OtherVpcAccountId" id="cdk-constructs.OtherAccountPeeringConfig.property.otherVpcAccountId"></a>

```go
OtherVpcAccountId *string
```

- *Type:* *string

VPC to be peered account's ID.

---

##### `OtherVpcCidr`<sup>Required</sup> <a name="OtherVpcCidr" id="cdk-constructs.OtherAccountPeeringConfig.property.otherVpcCidr"></a>

```go
OtherVpcCidr *string
```

- *Type:* *string

VPC to be peered mnemonic Id.

---

##### `OtherVpcId`<sup>Required</sup> <a name="OtherVpcId" id="cdk-constructs.OtherAccountPeeringConfig.property.otherVpcId"></a>

```go
OtherVpcId *string
```

- *Type:* *string

VPC to be peered vpcId.

---

##### `OtherVpcRegion`<sup>Required</sup> <a name="OtherVpcRegion" id="cdk-constructs.OtherAccountPeeringConfig.property.otherVpcRegion"></a>

```go
OtherVpcRegion *string
```

- *Type:* *string

VPC to be peered region.

---

##### `UniquePeeringId`<sup>Required</sup> <a name="UniquePeeringId" id="cdk-constructs.OtherAccountPeeringConfig.property.uniquePeeringId"></a>

```go
UniquePeeringId *string
```

- *Type:* *string

VPC to be peered mnemonic Id.

---

### PeeringConfig <a name="PeeringConfig" id="cdk-constructs.PeeringConfig"></a>

Route to add to the route tables, pointing to an already paired VPC.

#### Initializer <a name="Initializer" id="cdk-constructs.PeeringConfig.Initializer"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

&cdkconstructs.PeeringConfig {
	OtherVpc: github.com/aws/aws-cdk-go/awscdk/v2.aws_ec2.IVpc,
	PeeringId: *string,
}
```

#### Properties <a name="Properties" id="Properties"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.PeeringConfig.property.otherVpc">OtherVpc</a></code> | <code>github.com/aws/aws-cdk-go/awscdk/v2.aws_ec2.IVpc</code> | Id of vpc peering. |
| <code><a href="#cdk-constructs.PeeringConfig.property.peeringId">PeeringId</a></code> | <code>*string</code> | Unique id for this route. |

---

##### `OtherVpc`<sup>Required</sup> <a name="OtherVpc" id="cdk-constructs.PeeringConfig.property.otherVpc"></a>

```go
OtherVpc IVpc
```

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_ec2.IVpc

Id of vpc peering.

---

##### `PeeringId`<sup>Required</sup> <a name="PeeringId" id="cdk-constructs.PeeringConfig.property.peeringId"></a>

```go
PeeringId *string
```

- *Type:* *string

Unique id for this route.

---

### ProjectPreset <a name="ProjectPreset" id="cdk-constructs.ProjectPreset"></a>

#### Initializer <a name="Initializer" id="cdk-constructs.ProjectPreset.Initializer"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

&cdkconstructs.ProjectPreset {
	RepositoryBranchTagOrSha: *string,
	RepositoryName: *string,
	RepositoryRegion: *string,
	SubConfigs: *[]git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs.ProjectSubConfig,
}
```

#### Properties <a name="Properties" id="Properties"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.ProjectPreset.property.repositoryBranchTagOrSha">RepositoryBranchTagOrSha</a></code> | <code>*string</code> | *No description.* |
| <code><a href="#cdk-constructs.ProjectPreset.property.repositoryName">RepositoryName</a></code> | <code>*string</code> | *No description.* |
| <code><a href="#cdk-constructs.ProjectPreset.property.repositoryRegion">RepositoryRegion</a></code> | <code>*string</code> | *No description.* |
| <code><a href="#cdk-constructs.ProjectPreset.property.subConfigs">SubConfigs</a></code> | <code>*[]<a href="#cdk-constructs.ProjectSubConfig">ProjectSubConfig</a></code> | *No description.* |

---

##### `RepositoryBranchTagOrSha`<sup>Required</sup> <a name="RepositoryBranchTagOrSha" id="cdk-constructs.ProjectPreset.property.repositoryBranchTagOrSha"></a>

```go
RepositoryBranchTagOrSha *string
```

- *Type:* *string

---

##### `RepositoryName`<sup>Required</sup> <a name="RepositoryName" id="cdk-constructs.ProjectPreset.property.repositoryName"></a>

```go
RepositoryName *string
```

- *Type:* *string

---

##### `RepositoryRegion`<sup>Required</sup> <a name="RepositoryRegion" id="cdk-constructs.ProjectPreset.property.repositoryRegion"></a>

```go
RepositoryRegion *string
```

- *Type:* *string

---

##### `SubConfigs`<sup>Required</sup> <a name="SubConfigs" id="cdk-constructs.ProjectPreset.property.subConfigs"></a>

```go
SubConfigs *[]ProjectSubConfig
```

- *Type:* *[]<a href="#cdk-constructs.ProjectSubConfig">ProjectSubConfig</a>

---

### ProjectSubConfig <a name="ProjectSubConfig" id="cdk-constructs.ProjectSubConfig"></a>

#### Initializer <a name="Initializer" id="cdk-constructs.ProjectSubConfig.Initializer"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

&cdkconstructs.ProjectSubConfig {
	ReplaceValue: *string,
	SearchValue: *string,
}
```

#### Properties <a name="Properties" id="Properties"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.ProjectSubConfig.property.replaceValue">ReplaceValue</a></code> | <code>*string</code> | *No description.* |
| <code><a href="#cdk-constructs.ProjectSubConfig.property.searchValue">SearchValue</a></code> | <code>*string</code> | *No description.* |

---

##### `ReplaceValue`<sup>Required</sup> <a name="ReplaceValue" id="cdk-constructs.ProjectSubConfig.property.replaceValue"></a>

```go
ReplaceValue *string
```

- *Type:* *string

---

##### `SearchValue`<sup>Required</sup> <a name="SearchValue" id="cdk-constructs.ProjectSubConfig.property.searchValue"></a>

```go
SearchValue *string
```

- *Type:* *string

---

### SsmParameterReaderProps <a name="SsmParameterReaderProps" id="cdk-constructs.SsmParameterReaderProps"></a>

SSMParameter Reader Configuration.

#### Initializer <a name="Initializer" id="cdk-constructs.SsmParameterReaderProps.Initializer"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

&cdkconstructs.SsmParameterReaderProps {
	ParameterName: *string,
}
```

#### Properties <a name="Properties" id="Properties"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.SsmParameterReaderProps.property.parameterName">ParameterName</a></code> | <code>*string</code> | Complete name of the ssm parameter you want to read. |

---

##### `ParameterName`<sup>Required</sup> <a name="ParameterName" id="cdk-constructs.SsmParameterReaderProps.property.parameterName"></a>

```go
ParameterName *string
```

- *Type:* *string

Complete name of the ssm parameter you want to read.

---

### StageProducts <a name="StageProducts" id="cdk-constructs.StageProducts"></a>

#### Initializer <a name="Initializer" id="cdk-constructs.StageProducts.Initializer"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

&cdkconstructs.StageProducts {
	Actions: *[]github.com/aws/aws-cdk-go/awscdk/v2.aws_codepipeline_actions.Action,
	BuildProjects: *[]git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs.ThronPipelineBuildProject,
	Name: *string,
}
```

#### Properties <a name="Properties" id="Properties"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.StageProducts.property.actions">Actions</a></code> | <code>*[]github.com/aws/aws-cdk-go/awscdk/v2.aws_codepipeline_actions.Action</code> | *No description.* |
| <code><a href="#cdk-constructs.StageProducts.property.buildProjects">BuildProjects</a></code> | <code>*[]<a href="#cdk-constructs.ThronPipelineBuildProject">ThronPipelineBuildProject</a></code> | *No description.* |
| <code><a href="#cdk-constructs.StageProducts.property.name">Name</a></code> | <code>*string</code> | *No description.* |

---

##### `Actions`<sup>Required</sup> <a name="Actions" id="cdk-constructs.StageProducts.property.actions"></a>

```go
Actions *[]Action
```

- *Type:* *[]github.com/aws/aws-cdk-go/awscdk/v2.aws_codepipeline_actions.Action

---

##### `BuildProjects`<sup>Required</sup> <a name="BuildProjects" id="cdk-constructs.StageProducts.property.buildProjects"></a>

```go
BuildProjects *[]ThronPipelineBuildProject
```

- *Type:* *[]<a href="#cdk-constructs.ThronPipelineBuildProject">ThronPipelineBuildProject</a>

---

##### `Name`<sup>Required</sup> <a name="Name" id="cdk-constructs.StageProducts.property.name"></a>

```go
Name *string
```

- *Type:* *string

---

### StepConfig <a name="StepConfig" id="cdk-constructs.StepConfig"></a>

Custom overrides for each single action in the pipeline.

#### Initializer <a name="Initializer" id="cdk-constructs.StepConfig.Initializer"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

&cdkconstructs.StepConfig {
	ComputeType: github.com/aws/aws-cdk-go/awscdk/v2.aws_codebuild.ComputeType,
	CustomBuildImage: github.com/aws/aws-cdk-go/awscdk/v2.aws_codebuild.IBuildImage,
	EnvironmentalVariables: *map[string]github.com/aws/aws-cdk-go/awscdk/v2.aws_codebuild.BuildEnvironmentVariable,
}
```

#### Properties <a name="Properties" id="Properties"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.StepConfig.property.computeType">ComputeType</a></code> | <code>github.com/aws/aws-cdk-go/awscdk/v2.aws_codebuild.ComputeType</code> | Specify the size of the build containers. See https://docs.aws.amazon.com/codebuild/latest/userguide/build-env-ref-compute-types.html#environment.types for reference. |
| <code><a href="#cdk-constructs.StepConfig.property.customBuildImage">CustomBuildImage</a></code> | <code>github.com/aws/aws-cdk-go/awscdk/v2.aws_codebuild.IBuildImage</code> | Build image to be used fot this step. |
| <code><a href="#cdk-constructs.StepConfig.property.environmentalVariables">EnvironmentalVariables</a></code> | <code>*map[string]github.com/aws/aws-cdk-go/awscdk/v2.aws_codebuild.BuildEnvironmentVariable</code> | Map of additional env vars to pass to the build container. |

---

##### `ComputeType`<sup>Optional</sup> <a name="ComputeType" id="cdk-constructs.StepConfig.property.computeType"></a>

```go
ComputeType ComputeType
```

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_codebuild.ComputeType

Specify the size of the build containers. See https://docs.aws.amazon.com/codebuild/latest/userguide/build-env-ref-compute-types.html#environment.types for reference.

Defaults to `ComputeType.SMALL`

---

##### `CustomBuildImage`<sup>Optional</sup> <a name="CustomBuildImage" id="cdk-constructs.StepConfig.property.customBuildImage"></a>

```go
CustomBuildImage IBuildImage
```

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_codebuild.IBuildImage

Build image to be used fot this step.

---

##### `EnvironmentalVariables`<sup>Optional</sup> <a name="EnvironmentalVariables" id="cdk-constructs.StepConfig.property.environmentalVariables"></a>

```go
EnvironmentalVariables *map[string]BuildEnvironmentVariable
```

- *Type:* *map[string]github.com/aws/aws-cdk-go/awscdk/v2.aws_codebuild.BuildEnvironmentVariable

Map of additional env vars to pass to the build container.

---

### SubnetConfigProps <a name="SubnetConfigProps" id="cdk-constructs.SubnetConfigProps"></a>

Configuration to create a new subnet.

#### Initializer <a name="Initializer" id="cdk-constructs.SubnetConfigProps.Initializer"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

&cdkconstructs.SubnetConfigProps {
	AvailabilityZone: git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs.AvailabilityZone,
	Ipv4Cidr: *string,
	Ipv6CidrSlotNumber: *f64,
	Type: git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs.SubnetType,
}
```

#### Properties <a name="Properties" id="Properties"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.SubnetConfigProps.property.availabilityZone">AvailabilityZone</a></code> | <code><a href="#cdk-constructs.AvailabilityZone">AvailabilityZone</a></code> | The AZ in which to place the subnet. |
| <code><a href="#cdk-constructs.SubnetConfigProps.property.ipv4Cidr">Ipv4Cidr</a></code> | <code>*string</code> | The ipv4 CIDR block to be assigned to this subnet. |
| <code><a href="#cdk-constructs.SubnetConfigProps.property.ipv6CidrSlotNumber">Ipv6CidrSlotNumber</a></code> | <code>*f64</code> | The ipv6 CIDR block to assigned to this subnet (1-255). |
| <code><a href="#cdk-constructs.SubnetConfigProps.property.type">Type</a></code> | <code><a href="#cdk-constructs.SubnetType">SubnetType</a></code> | Whether the subnet is public or private. |

---

##### `AvailabilityZone`<sup>Required</sup> <a name="AvailabilityZone" id="cdk-constructs.SubnetConfigProps.property.availabilityZone"></a>

```go
AvailabilityZone AvailabilityZone
```

- *Type:* <a href="#cdk-constructs.AvailabilityZone">AvailabilityZone</a>

The AZ in which to place the subnet.

---

##### `Ipv4Cidr`<sup>Required</sup> <a name="Ipv4Cidr" id="cdk-constructs.SubnetConfigProps.property.ipv4Cidr"></a>

```go
Ipv4Cidr *string
```

- *Type:* *string

The ipv4 CIDR block to be assigned to this subnet.

---

##### `Ipv6CidrSlotNumber`<sup>Required</sup> <a name="Ipv6CidrSlotNumber" id="cdk-constructs.SubnetConfigProps.property.ipv6CidrSlotNumber"></a>

```go
Ipv6CidrSlotNumber *f64
```

- *Type:* *f64

The ipv6 CIDR block to assigned to this subnet (1-255).

The assigned slot is a /64 by convention

The assigned slot is derived from the automatically assigned /56 VPC CIDR block.

---

##### `Type`<sup>Required</sup> <a name="Type" id="cdk-constructs.SubnetConfigProps.property.type"></a>

```go
Type SubnetType
```

- *Type:* <a href="#cdk-constructs.SubnetType">SubnetType</a>

Whether the subnet is public or private.

---

### ThronAcmCertificateProps <a name="ThronAcmCertificateProps" id="cdk-constructs.ThronAcmCertificateProps"></a>

#### Initializer <a name="Initializer" id="cdk-constructs.ThronAcmCertificateProps.Initializer"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

&cdkconstructs.ThronAcmCertificateProps {
	DomainName: *string,
	Region: *string,
	SubjectAlternativeNames: *[]*string,
}
```

#### Properties <a name="Properties" id="Properties"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.ThronAcmCertificateProps.property.domainName">DomainName</a></code> | <code>*string</code> | FQDN to issue the certificate for. |
| <code><a href="#cdk-constructs.ThronAcmCertificateProps.property.region">Region</a></code> | <code>*string</code> | Region where to create the certificate, defaults to main stack region. |
| <code><a href="#cdk-constructs.ThronAcmCertificateProps.property.subjectAlternativeNames">SubjectAlternativeNames</a></code> | <code>*[]*string</code> | Alternative domain names on the certificate. |

---

##### `DomainName`<sup>Required</sup> <a name="DomainName" id="cdk-constructs.ThronAcmCertificateProps.property.domainName"></a>

```go
DomainName *string
```

- *Type:* *string

FQDN to issue the certificate for.

---

##### `Region`<sup>Optional</sup> <a name="Region" id="cdk-constructs.ThronAcmCertificateProps.property.region"></a>

```go
Region *string
```

- *Type:* *string

Region where to create the certificate, defaults to main stack region.

---

##### `SubjectAlternativeNames`<sup>Optional</sup> <a name="SubjectAlternativeNames" id="cdk-constructs.ThronAcmCertificateProps.property.subjectAlternativeNames"></a>

```go
SubjectAlternativeNames *[]*string
```

- *Type:* *[]*string

Alternative domain names on the certificate.

---

### ThronApiGatewayApiProps <a name="ThronApiGatewayApiProps" id="cdk-constructs.ThronApiGatewayApiProps"></a>

#### Initializer <a name="Initializer" id="cdk-constructs.ThronApiGatewayApiProps.Initializer"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

&cdkconstructs.ThronApiGatewayApiProps {
	MainDomain: *string,
}
```

#### Properties <a name="Properties" id="Properties"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.ThronApiGatewayApiProps.property.mainDomain">MainDomain</a></code> | <code>*string</code> | The main domain of the api gateway api, **without the cdn part**. |

---

##### `MainDomain`<sup>Required</sup> <a name="MainDomain" id="cdk-constructs.ThronApiGatewayApiProps.property.mainDomain"></a>

```go
MainDomain *string
```

- *Type:* *string

The main domain of the api gateway api, **without the cdn part**.

I.e `awsd04-product-api-adv1-productimports`

---

### ThronApiGatewayDomainAliasProps <a name="ThronApiGatewayDomainAliasProps" id="cdk-constructs.ThronApiGatewayDomainAliasProps"></a>

Properties to instantiate a new ThronDomainAlias.

#### Initializer <a name="Initializer" id="cdk-constructs.ThronApiGatewayDomainAliasProps.Initializer"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

&cdkconstructs.ThronApiGatewayDomainAliasProps {
	ApiGatewayApi: github.com/aws/aws-cdk-go/awscdk/v2.aws_apigateway.IRestApi,
	DomainName: *string,
	Prefix: *string,
}
```

#### Properties <a name="Properties" id="Properties"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.ThronApiGatewayDomainAliasProps.property.apiGatewayApi">ApiGatewayApi</a></code> | <code>github.com/aws/aws-cdk-go/awscdk/v2.aws_apigateway.IRestApi</code> | API to create the alias to. |
| <code><a href="#cdk-constructs.ThronApiGatewayDomainAliasProps.property.domainName">DomainName</a></code> | <code>*string</code> | Domain name to alias the API Gateway Endpoint to. |
| <code><a href="#cdk-constructs.ThronApiGatewayDomainAliasProps.property.prefix">Prefix</a></code> | <code>*string</code> | Unique id to add to CFN ids to prevent the first synth from failing. |

---

##### `ApiGatewayApi`<sup>Required</sup> <a name="ApiGatewayApi" id="cdk-constructs.ThronApiGatewayDomainAliasProps.property.apiGatewayApi"></a>

```go
ApiGatewayApi IRestApi
```

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_apigateway.IRestApi

API to create the alias to.

---

##### `DomainName`<sup>Required</sup> <a name="DomainName" id="cdk-constructs.ThronApiGatewayDomainAliasProps.property.domainName"></a>

```go
DomainName *string
```

- *Type:* *string

Domain name to alias the API Gateway Endpoint to.

---

##### `Prefix`<sup>Required</sup> <a name="Prefix" id="cdk-constructs.ThronApiGatewayDomainAliasProps.property.prefix"></a>

```go
Prefix *string
```

- *Type:* *string

Unique id to add to CFN ids to prevent the first synth from failing.

---

### ThronCachePolicyProps <a name="ThronCachePolicyProps" id="cdk-constructs.ThronCachePolicyProps"></a>

#### Initializer <a name="Initializer" id="cdk-constructs.ThronCachePolicyProps.Initializer"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

&cdkconstructs.ThronCachePolicyProps {
	DefaultTtl: github.com/aws/aws-cdk-go/awscdk/v2.Duration,
	MaxTtl: github.com/aws/aws-cdk-go/awscdk/v2.Duration,
	MinTtl: github.com/aws/aws-cdk-go/awscdk/v2.Duration,
}
```

#### Properties <a name="Properties" id="Properties"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.ThronCachePolicyProps.property.defaultTtl">DefaultTtl</a></code> | <code>github.com/aws/aws-cdk-go/awscdk/v2.Duration</code> | *No description.* |
| <code><a href="#cdk-constructs.ThronCachePolicyProps.property.maxTtl">MaxTtl</a></code> | <code>github.com/aws/aws-cdk-go/awscdk/v2.Duration</code> | *No description.* |
| <code><a href="#cdk-constructs.ThronCachePolicyProps.property.minTtl">MinTtl</a></code> | <code>github.com/aws/aws-cdk-go/awscdk/v2.Duration</code> | *No description.* |

---

##### `DefaultTtl`<sup>Optional</sup> <a name="DefaultTtl" id="cdk-constructs.ThronCachePolicyProps.property.defaultTtl"></a>

```go
DefaultTtl Duration
```

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.Duration

---

##### `MaxTtl`<sup>Optional</sup> <a name="MaxTtl" id="cdk-constructs.ThronCachePolicyProps.property.maxTtl"></a>

```go
MaxTtl Duration
```

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.Duration

---

##### `MinTtl`<sup>Optional</sup> <a name="MinTtl" id="cdk-constructs.ThronCachePolicyProps.property.minTtl"></a>

```go
MinTtl Duration
```

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.Duration

---

### ThronCloudFrontDistributionProps <a name="ThronCloudFrontDistributionProps" id="cdk-constructs.ThronCloudFrontDistributionProps"></a>

#### Initializer <a name="Initializer" id="cdk-constructs.ThronCloudFrontDistributionProps.Initializer"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

&cdkconstructs.ThronCloudFrontDistributionProps {
	DomainName: *string,
	Source: *string,
	CachePolicy: git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs.ThronCachePolicy,
	DefaultRootObject: *string,
	DefaultRootObjectCachePolicy: git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs.ThronCachePolicy,
	DefaultRootObjectResponseHeaderPolicy: git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs.ThronResponseHeaderPolicy,
	Description: *string,
	Prune: *bool,
	ResponseHeaderPolicy: git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs.ThronResponseHeaderPolicy,
	Version: *string,
}
```

#### Properties <a name="Properties" id="Properties"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.ThronCloudFrontDistributionProps.property.domainName">DomainName</a></code> | <code>*string</code> | Validated FQDN. |
| <code><a href="#cdk-constructs.ThronCloudFrontDistributionProps.property.source">Source</a></code> | <code>*string</code> | Source path from which to deploy the contents of frontend. |
| <code><a href="#cdk-constructs.ThronCloudFrontDistributionProps.property.cachePolicy">CachePolicy</a></code> | <code><a href="#cdk-constructs.ThronCachePolicy">ThronCachePolicy</a></code> | CloudFront's Cache Policy to use on the distribution. |
| <code><a href="#cdk-constructs.ThronCloudFrontDistributionProps.property.defaultRootObject">DefaultRootObject</a></code> | <code>*string</code> | Object that you want CloudFront to request from your origin when a user requests the root URL for your distribution. |
| <code><a href="#cdk-constructs.ThronCloudFrontDistributionProps.property.defaultRootObjectCachePolicy">DefaultRootObjectCachePolicy</a></code> | <code><a href="#cdk-constructs.ThronCachePolicy">ThronCachePolicy</a></code> | *No description.* |
| <code><a href="#cdk-constructs.ThronCloudFrontDistributionProps.property.defaultRootObjectResponseHeaderPolicy">DefaultRootObjectResponseHeaderPolicy</a></code> | <code><a href="#cdk-constructs.ThronResponseHeaderPolicy">ThronResponseHeaderPolicy</a></code> | CloudFront's Response Header Policy to use on the distribution. |
| <code><a href="#cdk-constructs.ThronCloudFrontDistributionProps.property.description">Description</a></code> | <code>*string</code> | Description of the cloudfront distribution; |
| <code><a href="#cdk-constructs.ThronCloudFrontDistributionProps.property.prune">Prune</a></code> | <code>*bool</code> | If this is set to false, files in the destination bucket that do not exist in the asset, will NOT be deleted during deployment (create/update). |
| <code><a href="#cdk-constructs.ThronCloudFrontDistributionProps.property.responseHeaderPolicy">ResponseHeaderPolicy</a></code> | <code><a href="#cdk-constructs.ThronResponseHeaderPolicy">ThronResponseHeaderPolicy</a></code> | CloudFront's Response Header Policy to use on the distribution. |
| <code><a href="#cdk-constructs.ThronCloudFrontDistributionProps.property.version">Version</a></code> | <code>*string</code> | Prefix key used for versioning the s3 deployment bucket. |

---

##### `DomainName`<sup>Required</sup> <a name="DomainName" id="cdk-constructs.ThronCloudFrontDistributionProps.property.domainName"></a>

```go
DomainName *string
```

- *Type:* *string

Validated FQDN.

---

##### `Source`<sup>Required</sup> <a name="Source" id="cdk-constructs.ThronCloudFrontDistributionProps.property.source"></a>

```go
Source *string
```

- *Type:* *string

Source path from which to deploy the contents of frontend.

---

##### `CachePolicy`<sup>Optional</sup> <a name="CachePolicy" id="cdk-constructs.ThronCloudFrontDistributionProps.property.cachePolicy"></a>

```go
CachePolicy ThronCachePolicy
```

- *Type:* <a href="#cdk-constructs.ThronCachePolicy">ThronCachePolicy</a>

CloudFront's Cache Policy to use on the distribution.

---

##### `DefaultRootObject`<sup>Optional</sup> <a name="DefaultRootObject" id="cdk-constructs.ThronCloudFrontDistributionProps.property.defaultRootObject"></a>

```go
DefaultRootObject *string
```

- *Type:* *string

Object that you want CloudFront to request from your origin when a user requests the root URL for your distribution.

---

##### `DefaultRootObjectCachePolicy`<sup>Optional</sup> <a name="DefaultRootObjectCachePolicy" id="cdk-constructs.ThronCloudFrontDistributionProps.property.defaultRootObjectCachePolicy"></a>

```go
DefaultRootObjectCachePolicy ThronCachePolicy
```

- *Type:* <a href="#cdk-constructs.ThronCachePolicy">ThronCachePolicy</a>

---

##### `DefaultRootObjectResponseHeaderPolicy`<sup>Optional</sup> <a name="DefaultRootObjectResponseHeaderPolicy" id="cdk-constructs.ThronCloudFrontDistributionProps.property.defaultRootObjectResponseHeaderPolicy"></a>

```go
DefaultRootObjectResponseHeaderPolicy ThronResponseHeaderPolicy
```

- *Type:* <a href="#cdk-constructs.ThronResponseHeaderPolicy">ThronResponseHeaderPolicy</a>

CloudFront's Response Header Policy to use on the distribution.

---

##### `Description`<sup>Optional</sup> <a name="Description" id="cdk-constructs.ThronCloudFrontDistributionProps.property.description"></a>

```go
Description *string
```

- *Type:* *string

Description of the cloudfront distribution;

defaults to `domainName`

---

##### `Prune`<sup>Optional</sup> <a name="Prune" id="cdk-constructs.ThronCloudFrontDistributionProps.property.prune"></a>

```go
Prune *bool
```

- *Type:* *bool
- *Default:* true

If this is set to false, files in the destination bucket that do not exist in the asset, will NOT be deleted during deployment (create/update).

---

##### `ResponseHeaderPolicy`<sup>Optional</sup> <a name="ResponseHeaderPolicy" id="cdk-constructs.ThronCloudFrontDistributionProps.property.responseHeaderPolicy"></a>

```go
ResponseHeaderPolicy ThronResponseHeaderPolicy
```

- *Type:* <a href="#cdk-constructs.ThronResponseHeaderPolicy">ThronResponseHeaderPolicy</a>

CloudFront's Response Header Policy to use on the distribution.

---

##### `Version`<sup>Optional</sup> <a name="Version" id="cdk-constructs.ThronCloudFrontDistributionProps.property.version"></a>

```go
Version *string
```

- *Type:* *string

Prefix key used for versioning the s3 deployment bucket.

---

### ThronCreatedApiGatewayEndpoint <a name="ThronCreatedApiGatewayEndpoint" id="cdk-constructs.ThronCreatedApiGatewayEndpoint"></a>

#### Initializer <a name="Initializer" id="cdk-constructs.ThronCreatedApiGatewayEndpoint.Initializer"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

&cdkconstructs.ThronCreatedApiGatewayEndpoint {
	ApiGatewayApi: git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs.ThronApiGatewayApi,
	FullEndpoint: *string,
	MainDomain: *string,
	Path: *string,
}
```

#### Properties <a name="Properties" id="Properties"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.ThronCreatedApiGatewayEndpoint.property.apiGatewayApi">ApiGatewayApi</a></code> | <code><a href="#cdk-constructs.ThronApiGatewayApi">ThronApiGatewayApi</a></code> | The ThronApiGatewayApi associated with the endpoint. |
| <code><a href="#cdk-constructs.ThronCreatedApiGatewayEndpoint.property.fullEndpoint">FullEndpoint</a></code> | <code>*string</code> | The full uri of the exposed api endpoint, i.e `awsd04-product-api-adv1-productimports.4me.cdndev.weebo.it/api/adv1/productimports/`. |
| <code><a href="#cdk-constructs.ThronCreatedApiGatewayEndpoint.property.mainDomain">MainDomain</a></code> | <code>*string</code> | The main domain of the api gateway endpoint, i.e `awsd04-product-api-adv1-productimports.4me.cdndev.weebo.it`. |
| <code><a href="#cdk-constructs.ThronCreatedApiGatewayEndpoint.property.path">Path</a></code> | <code>*string</code> | The path of the exposed api endpoint, i.e `/api/adv1/productimports/`. |

---

##### `ApiGatewayApi`<sup>Required</sup> <a name="ApiGatewayApi" id="cdk-constructs.ThronCreatedApiGatewayEndpoint.property.apiGatewayApi"></a>

```go
ApiGatewayApi ThronApiGatewayApi
```

- *Type:* <a href="#cdk-constructs.ThronApiGatewayApi">ThronApiGatewayApi</a>

The ThronApiGatewayApi associated with the endpoint.

---

##### `FullEndpoint`<sup>Required</sup> <a name="FullEndpoint" id="cdk-constructs.ThronCreatedApiGatewayEndpoint.property.fullEndpoint"></a>

```go
FullEndpoint *string
```

- *Type:* *string

The full uri of the exposed api endpoint, i.e `awsd04-product-api-adv1-productimports.4me.cdndev.weebo.it/api/adv1/productimports/`.

---

##### `MainDomain`<sup>Required</sup> <a name="MainDomain" id="cdk-constructs.ThronCreatedApiGatewayEndpoint.property.mainDomain"></a>

```go
MainDomain *string
```

- *Type:* *string

The main domain of the api gateway endpoint, i.e `awsd04-product-api-adv1-productimports.4me.cdndev.weebo.it`.

---

##### `Path`<sup>Required</sup> <a name="Path" id="cdk-constructs.ThronCreatedApiGatewayEndpoint.property.path"></a>

```go
Path *string
```

- *Type:* *string

The path of the exposed api endpoint, i.e `/api/adv1/productimports/`.

---

### ThronEc2ServiceProps <a name="ThronEc2ServiceProps" id="cdk-constructs.ThronEc2ServiceProps"></a>

#### Initializer <a name="Initializer" id="cdk-constructs.ThronEc2ServiceProps.Initializer"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

&cdkconstructs.ThronEc2ServiceProps {
	Cpu: *f64,
	Ram: *f64,
	ContainerImage: github.com/aws/aws-cdk-go/awscdk/v2.aws_ecs.ContainerImage,
	Environment: *map[string]*string,
	Port: *f64,
	PrometheusMetricsPath: *string,
	Secrets: *map[string]github.com/aws/aws-cdk-go/awscdk/v2.aws_ecs.Secret,
	Cluster: git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs.ClusterOption,
	DockerContextPath: *string,
	DockerfileName: *string,
	Endpoints: *map[string]git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs.ThronEndpointAlbProps,
	HealthCheck: github.com/aws/aws-cdk-go/awscdk/v2.aws_elasticloadbalancingv2.HealthCheck,
	LegacyEndpoints: *map[string]git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs.LegacyEndpointAlbProps,
	TargetScaling: git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs.ThronTargetScalingProps,
}
```

#### Properties <a name="Properties" id="Properties"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.ThronEc2ServiceProps.property.cpu">Cpu</a></code> | <code>*f64</code> | The number of cpu units used by the task. |
| <code><a href="#cdk-constructs.ThronEc2ServiceProps.property.ram">Ram</a></code> | <code>*f64</code> | The amount (in MiB) of memory used by the task. |
| <code><a href="#cdk-constructs.ThronEc2ServiceProps.property.containerImage">ContainerImage</a></code> | <code>github.com/aws/aws-cdk-go/awscdk/v2.aws_ecs.ContainerImage</code> | Container image to use for the container. |
| <code><a href="#cdk-constructs.ThronEc2ServiceProps.property.environment">Environment</a></code> | <code>*map[string]*string</code> | The environment variables to pass to the container. |
| <code><a href="#cdk-constructs.ThronEc2ServiceProps.property.port">Port</a></code> | <code>*f64</code> | The port exposed for connection. |
| <code><a href="#cdk-constructs.ThronEc2ServiceProps.property.prometheusMetricsPath">PrometheusMetricsPath</a></code> | <code>*string</code> | Path where Prometheus metrics are exposed. |
| <code><a href="#cdk-constructs.ThronEc2ServiceProps.property.secrets">Secrets</a></code> | <code>*map[string]github.com/aws/aws-cdk-go/awscdk/v2.aws_ecs.Secret</code> | The secrets to pass to the container (got by valueFrom). |
| <code><a href="#cdk-constructs.ThronEc2ServiceProps.property.cluster">Cluster</a></code> | <code><a href="#cdk-constructs.ClusterOption">ClusterOption</a></code> | *No description.* |
| <code><a href="#cdk-constructs.ThronEc2ServiceProps.property.dockerContextPath">DockerContextPath</a></code> | <code>*string</code> | Context of docker build. |
| <code><a href="#cdk-constructs.ThronEc2ServiceProps.property.dockerfileName">DockerfileName</a></code> | <code>*string</code> | Name of Dockerfile. |
| <code><a href="#cdk-constructs.ThronEc2ServiceProps.property.endpoints">Endpoints</a></code> | <code>*map[string]<a href="#cdk-constructs.ThronEndpointAlbProps">ThronEndpointAlbProps</a></code> | Endpoints associated with this service. |
| <code><a href="#cdk-constructs.ThronEc2ServiceProps.property.healthCheck">HealthCheck</a></code> | <code>github.com/aws/aws-cdk-go/awscdk/v2.aws_elasticloadbalancingv2.HealthCheck</code> | Default healthcheck override. |
| <code><a href="#cdk-constructs.ThronEc2ServiceProps.property.legacyEndpoints">LegacyEndpoints</a></code> | <code>*map[string]<a href="#cdk-constructs.LegacyEndpointAlbProps">LegacyEndpointAlbProps</a></code> | Legacy endpoints associated with this service. |
| <code><a href="#cdk-constructs.ThronEc2ServiceProps.property.targetScaling">TargetScaling</a></code> | <code><a href="#cdk-constructs.ThronTargetScalingProps">ThronTargetScalingProps</a></code> | *No description.* |

---

##### `Cpu`<sup>Required</sup> <a name="Cpu" id="cdk-constructs.ThronEc2ServiceProps.property.cpu"></a>

```go
Cpu *f64
```

- *Type:* *f64

The number of cpu units used by the task.

---

##### `Ram`<sup>Required</sup> <a name="Ram" id="cdk-constructs.ThronEc2ServiceProps.property.ram"></a>

```go
Ram *f64
```

- *Type:* *f64

The amount (in MiB) of memory used by the task.

---

##### `ContainerImage`<sup>Optional</sup> <a name="ContainerImage" id="cdk-constructs.ThronEc2ServiceProps.property.containerImage"></a>

```go
ContainerImage ContainerImage
```

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_ecs.ContainerImage

Container image to use for the container.

---

##### `Environment`<sup>Optional</sup> <a name="Environment" id="cdk-constructs.ThronEc2ServiceProps.property.environment"></a>

```go
Environment *map[string]*string
```

- *Type:* *map[string]*string
- *Default:* No environment variables.

The environment variables to pass to the container.

---

##### `Port`<sup>Optional</sup> <a name="Port" id="cdk-constructs.ThronEc2ServiceProps.property.port"></a>

```go
Port *f64
```

- *Type:* *f64

The port exposed for connection.

---

##### `PrometheusMetricsPath`<sup>Optional</sup> <a name="PrometheusMetricsPath" id="cdk-constructs.ThronEc2ServiceProps.property.prometheusMetricsPath"></a>

```go
PrometheusMetricsPath *string
```

- *Type:* *string

Path where Prometheus metrics are exposed.

---

##### `Secrets`<sup>Optional</sup> <a name="Secrets" id="cdk-constructs.ThronEc2ServiceProps.property.secrets"></a>

```go
Secrets *map[string]Secret
```

- *Type:* *map[string]github.com/aws/aws-cdk-go/awscdk/v2.aws_ecs.Secret

The secrets to pass to the container (got by valueFrom).

---

##### `Cluster`<sup>Required</sup> <a name="Cluster" id="cdk-constructs.ThronEc2ServiceProps.property.cluster"></a>

```go
Cluster ClusterOption
```

- *Type:* <a href="#cdk-constructs.ClusterOption">ClusterOption</a>

---

##### `DockerContextPath`<sup>Required</sup> <a name="DockerContextPath" id="cdk-constructs.ThronEc2ServiceProps.property.dockerContextPath"></a>

```go
DockerContextPath *string
```

- *Type:* *string

Context of docker build.

---

##### `DockerfileName`<sup>Optional</sup> <a name="DockerfileName" id="cdk-constructs.ThronEc2ServiceProps.property.dockerfileName"></a>

```go
DockerfileName *string
```

- *Type:* *string
- *Default:* Dockerfile

Name of Dockerfile.

---

##### `Endpoints`<sup>Optional</sup> <a name="Endpoints" id="cdk-constructs.ThronEc2ServiceProps.property.endpoints"></a>

```go
Endpoints *map[string]ThronEndpointAlbProps
```

- *Type:* *map[string]<a href="#cdk-constructs.ThronEndpointAlbProps">ThronEndpointAlbProps</a>

Endpoints associated with this service.

---

##### `HealthCheck`<sup>Optional</sup> <a name="HealthCheck" id="cdk-constructs.ThronEc2ServiceProps.property.healthCheck"></a>

```go
HealthCheck HealthCheck
```

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_elasticloadbalancingv2.HealthCheck

Default healthcheck override.

---

##### `LegacyEndpoints`<sup>Optional</sup> <a name="LegacyEndpoints" id="cdk-constructs.ThronEc2ServiceProps.property.legacyEndpoints"></a>

```go
LegacyEndpoints *map[string]LegacyEndpointAlbProps
```

- *Type:* *map[string]<a href="#cdk-constructs.LegacyEndpointAlbProps">LegacyEndpointAlbProps</a>

Legacy endpoints associated with this service.

---

##### `TargetScaling`<sup>Optional</sup> <a name="TargetScaling" id="cdk-constructs.ThronEc2ServiceProps.property.targetScaling"></a>

```go
TargetScaling ThronTargetScalingProps
```

- *Type:* <a href="#cdk-constructs.ThronTargetScalingProps">ThronTargetScalingProps</a>

---

### ThronEc2TargetScalingProps <a name="ThronEc2TargetScalingProps" id="cdk-constructs.ThronEc2TargetScalingProps"></a>

#### Initializer <a name="Initializer" id="cdk-constructs.ThronEc2TargetScalingProps.Initializer"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

&cdkconstructs.ThronEc2TargetScalingProps {
	MaxCapacity: *f64,
	MinCapacity: *f64,
	TargetValue: *f64,
	PredefinedMetric: github.com/aws/aws-cdk-go/awscdk/v2.aws_applicationautoscaling.PredefinedMetric,
	ScaleInCooldown: github.com/aws/aws-cdk-go/awscdk/v2.Duration,
	ScaleOutCooldown: github.com/aws/aws-cdk-go/awscdk/v2.Duration,
	Ec2Service: github.com/aws/aws-cdk-go/awscdk/v2.aws_ecs.Ec2Service,
}
```

#### Properties <a name="Properties" id="Properties"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.ThronEc2TargetScalingProps.property.maxCapacity">MaxCapacity</a></code> | <code>*f64</code> | The maximum value that Application Auto Scaling can use to scale a target during a scaling activity. |
| <code><a href="#cdk-constructs.ThronEc2TargetScalingProps.property.minCapacity">MinCapacity</a></code> | <code>*f64</code> | The minimum value that Application Auto Scaling can use to scale a target during a scaling activity. |
| <code><a href="#cdk-constructs.ThronEc2TargetScalingProps.property.targetValue">TargetValue</a></code> | <code>*f64</code> | The target value for the metric. |
| <code><a href="#cdk-constructs.ThronEc2TargetScalingProps.property.predefinedMetric">PredefinedMetric</a></code> | <code>github.com/aws/aws-cdk-go/awscdk/v2.aws_applicationautoscaling.PredefinedMetric</code> | A predefined metric for application autoscaling. |
| <code><a href="#cdk-constructs.ThronEc2TargetScalingProps.property.scaleInCooldown">ScaleInCooldown</a></code> | <code>github.com/aws/aws-cdk-go/awscdk/v2.Duration</code> | The amount of time after a scale in activity completes before another scale in activity can start. |
| <code><a href="#cdk-constructs.ThronEc2TargetScalingProps.property.scaleOutCooldown">ScaleOutCooldown</a></code> | <code>github.com/aws/aws-cdk-go/awscdk/v2.Duration</code> | The amount of time after a scale in activity completes before another scale in activity can start. |
| <code><a href="#cdk-constructs.ThronEc2TargetScalingProps.property.ec2Service">Ec2Service</a></code> | <code>github.com/aws/aws-cdk-go/awscdk/v2.aws_ecs.Ec2Service</code> | Ec2 Service used as target resource. |

---

##### `MaxCapacity`<sup>Required</sup> <a name="MaxCapacity" id="cdk-constructs.ThronEc2TargetScalingProps.property.maxCapacity"></a>

```go
MaxCapacity *f64
```

- *Type:* *f64

The maximum value that Application Auto Scaling can use to scale a target during a scaling activity.

---

##### `MinCapacity`<sup>Required</sup> <a name="MinCapacity" id="cdk-constructs.ThronEc2TargetScalingProps.property.minCapacity"></a>

```go
MinCapacity *f64
```

- *Type:* *f64

The minimum value that Application Auto Scaling can use to scale a target during a scaling activity.

---

##### `TargetValue`<sup>Required</sup> <a name="TargetValue" id="cdk-constructs.ThronEc2TargetScalingProps.property.targetValue"></a>

```go
TargetValue *f64
```

- *Type:* *f64

The target value for the metric.

---

##### `PredefinedMetric`<sup>Optional</sup> <a name="PredefinedMetric" id="cdk-constructs.ThronEc2TargetScalingProps.property.predefinedMetric"></a>

```go
PredefinedMetric PredefinedMetric
```

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_applicationautoscaling.PredefinedMetric

A predefined metric for application autoscaling.

The metric must track utilization. Scaling out will happen if the metric is higher than the target value,
scaling in will happen in the metric is lower than the target value.

---

##### `ScaleInCooldown`<sup>Optional</sup> <a name="ScaleInCooldown" id="cdk-constructs.ThronEc2TargetScalingProps.property.scaleInCooldown"></a>

```go
ScaleInCooldown Duration
```

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.Duration
- *Default:* Duration.minutes(300)

The amount of time after a scale in activity completes before another scale in activity can start.

---

##### `ScaleOutCooldown`<sup>Optional</sup> <a name="ScaleOutCooldown" id="cdk-constructs.ThronEc2TargetScalingProps.property.scaleOutCooldown"></a>

```go
ScaleOutCooldown Duration
```

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.Duration
- *Default:* Duration.minutes(90)

The amount of time after a scale in activity completes before another scale in activity can start.

---

##### `Ec2Service`<sup>Required</sup> <a name="Ec2Service" id="cdk-constructs.ThronEc2TargetScalingProps.property.ec2Service"></a>

```go
Ec2Service Ec2Service
```

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_ecs.Ec2Service

Ec2 Service used as target resource.

---

### ThronEc2TaskDefinitionProps <a name="ThronEc2TaskDefinitionProps" id="cdk-constructs.ThronEc2TaskDefinitionProps"></a>

#### Initializer <a name="Initializer" id="cdk-constructs.ThronEc2TaskDefinitionProps.Initializer"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

&cdkconstructs.ThronEc2TaskDefinitionProps {
	Cpu: *f64,
	Ram: *f64,
	ContainerImage: github.com/aws/aws-cdk-go/awscdk/v2.aws_ecs.ContainerImage,
	Environment: *map[string]*string,
	Port: *f64,
	PrometheusMetricsPath: *string,
	Secrets: *map[string]github.com/aws/aws-cdk-go/awscdk/v2.aws_ecs.Secret,
}
```

#### Properties <a name="Properties" id="Properties"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.ThronEc2TaskDefinitionProps.property.cpu">Cpu</a></code> | <code>*f64</code> | The number of cpu units used by the task. |
| <code><a href="#cdk-constructs.ThronEc2TaskDefinitionProps.property.ram">Ram</a></code> | <code>*f64</code> | The amount (in MiB) of memory used by the task. |
| <code><a href="#cdk-constructs.ThronEc2TaskDefinitionProps.property.containerImage">ContainerImage</a></code> | <code>github.com/aws/aws-cdk-go/awscdk/v2.aws_ecs.ContainerImage</code> | Container image to use for the container. |
| <code><a href="#cdk-constructs.ThronEc2TaskDefinitionProps.property.environment">Environment</a></code> | <code>*map[string]*string</code> | The environment variables to pass to the container. |
| <code><a href="#cdk-constructs.ThronEc2TaskDefinitionProps.property.port">Port</a></code> | <code>*f64</code> | The port exposed for connection. |
| <code><a href="#cdk-constructs.ThronEc2TaskDefinitionProps.property.prometheusMetricsPath">PrometheusMetricsPath</a></code> | <code>*string</code> | Path where Prometheus metrics are exposed. |
| <code><a href="#cdk-constructs.ThronEc2TaskDefinitionProps.property.secrets">Secrets</a></code> | <code>*map[string]github.com/aws/aws-cdk-go/awscdk/v2.aws_ecs.Secret</code> | The secrets to pass to the container (got by valueFrom). |

---

##### `Cpu`<sup>Required</sup> <a name="Cpu" id="cdk-constructs.ThronEc2TaskDefinitionProps.property.cpu"></a>

```go
Cpu *f64
```

- *Type:* *f64

The number of cpu units used by the task.

---

##### `Ram`<sup>Required</sup> <a name="Ram" id="cdk-constructs.ThronEc2TaskDefinitionProps.property.ram"></a>

```go
Ram *f64
```

- *Type:* *f64

The amount (in MiB) of memory used by the task.

---

##### `ContainerImage`<sup>Optional</sup> <a name="ContainerImage" id="cdk-constructs.ThronEc2TaskDefinitionProps.property.containerImage"></a>

```go
ContainerImage ContainerImage
```

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_ecs.ContainerImage

Container image to use for the container.

---

##### `Environment`<sup>Optional</sup> <a name="Environment" id="cdk-constructs.ThronEc2TaskDefinitionProps.property.environment"></a>

```go
Environment *map[string]*string
```

- *Type:* *map[string]*string
- *Default:* No environment variables.

The environment variables to pass to the container.

---

##### `Port`<sup>Optional</sup> <a name="Port" id="cdk-constructs.ThronEc2TaskDefinitionProps.property.port"></a>

```go
Port *f64
```

- *Type:* *f64

The port exposed for connection.

---

##### `PrometheusMetricsPath`<sup>Optional</sup> <a name="PrometheusMetricsPath" id="cdk-constructs.ThronEc2TaskDefinitionProps.property.prometheusMetricsPath"></a>

```go
PrometheusMetricsPath *string
```

- *Type:* *string

Path where Prometheus metrics are exposed.

---

##### `Secrets`<sup>Optional</sup> <a name="Secrets" id="cdk-constructs.ThronEc2TaskDefinitionProps.property.secrets"></a>

```go
Secrets *map[string]Secret
```

- *Type:* *map[string]github.com/aws/aws-cdk-go/awscdk/v2.aws_ecs.Secret

The secrets to pass to the container (got by valueFrom).

---

### ThronEndpointAlbProps <a name="ThronEndpointAlbProps" id="cdk-constructs.ThronEndpointAlbProps"></a>

#### Initializer <a name="Initializer" id="cdk-constructs.ThronEndpointAlbProps.Initializer"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

&cdkconstructs.ThronEndpointAlbProps {
	ServiceGroup: git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs.ServiceGroup,
	ServiceName: *string,
	Stack: github.com/aws/aws-cdk-go/awscdk/v2.Stack,
	Version: *f64,
	Visibility: git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs.EndpointVisibility,
}
```

#### Properties <a name="Properties" id="Properties"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.ThronEndpointAlbProps.property.serviceGroup">ServiceGroup</a></code> | <code><a href="#cdk-constructs.ServiceGroup">ServiceGroup</a></code> | Service group of the service. |
| <code><a href="#cdk-constructs.ThronEndpointAlbProps.property.serviceName">ServiceName</a></code> | <code>*string</code> | Name of the service the endpoint exposes. |
| <code><a href="#cdk-constructs.ThronEndpointAlbProps.property.stack">Stack</a></code> | <code>github.com/aws/aws-cdk-go/awscdk/v2.Stack</code> | The reference of parent Stack. |
| <code><a href="#cdk-constructs.ThronEndpointAlbProps.property.version">Version</a></code> | <code>*f64</code> | The version of the API exposed by the endpoint. |
| <code><a href="#cdk-constructs.ThronEndpointAlbProps.property.visibility">Visibility</a></code> | <code><a href="#cdk-constructs.EndpointVisibility">EndpointVisibility</a></code> | Wether the endpoint is private or public. |

---

##### `ServiceGroup`<sup>Required</sup> <a name="ServiceGroup" id="cdk-constructs.ThronEndpointAlbProps.property.serviceGroup"></a>

```go
ServiceGroup ServiceGroup
```

- *Type:* <a href="#cdk-constructs.ServiceGroup">ServiceGroup</a>

Service group of the service.

---

##### `ServiceName`<sup>Required</sup> <a name="ServiceName" id="cdk-constructs.ThronEndpointAlbProps.property.serviceName"></a>

```go
ServiceName *string
```

- *Type:* *string

Name of the service the endpoint exposes.

---

##### `Stack`<sup>Optional</sup> <a name="Stack" id="cdk-constructs.ThronEndpointAlbProps.property.stack"></a>

```go
Stack Stack
```

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.Stack

The reference of parent Stack.

---

##### `Version`<sup>Optional</sup> <a name="Version" id="cdk-constructs.ThronEndpointAlbProps.property.version"></a>

```go
Version *f64
```

- *Type:* *f64
- *Default:* 1

The version of the API exposed by the endpoint.

---

##### `Visibility`<sup>Optional</sup> <a name="Visibility" id="cdk-constructs.ThronEndpointAlbProps.property.visibility"></a>

```go
Visibility EndpointVisibility
```

- *Type:* <a href="#cdk-constructs.EndpointVisibility">EndpointVisibility</a>
- *Default:* EndpointVisibility.PRIVATE

Wether the endpoint is private or public.

---

### ThronEndpointApiGatewayProps <a name="ThronEndpointApiGatewayProps" id="cdk-constructs.ThronEndpointApiGatewayProps"></a>

#### Initializer <a name="Initializer" id="cdk-constructs.ThronEndpointApiGatewayProps.Initializer"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

&cdkconstructs.ThronEndpointApiGatewayProps {
	ApiGatewayApi: github.com/aws/aws-cdk-go/awscdk/v2.aws_apigateway.IRestApi,
	BasePath: *string,
	LambdaFunction: github.com/aws/aws-cdk-go/awscdk/v2.aws_lambda.IFunction,
	Timeout: github.com/aws/aws-cdk-go/awscdk/v2.Duration,
}
```

#### Properties <a name="Properties" id="Properties"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.ThronEndpointApiGatewayProps.property.apiGatewayApi">ApiGatewayApi</a></code> | <code>github.com/aws/aws-cdk-go/awscdk/v2.aws_apigateway.IRestApi</code> | The API on which the endpoint should be added. |
| <code><a href="#cdk-constructs.ThronEndpointApiGatewayProps.property.basePath">BasePath</a></code> | <code>*string</code> | The path on which to add the endpoint. |
| <code><a href="#cdk-constructs.ThronEndpointApiGatewayProps.property.lambdaFunction">LambdaFunction</a></code> | <code>github.com/aws/aws-cdk-go/awscdk/v2.aws_lambda.IFunction</code> | The function to attach to the endpoint. |
| <code><a href="#cdk-constructs.ThronEndpointApiGatewayProps.property.timeout">Timeout</a></code> | <code>github.com/aws/aws-cdk-go/awscdk/v2.Duration</code> | The timeout of the integration. |

---

##### `ApiGatewayApi`<sup>Required</sup> <a name="ApiGatewayApi" id="cdk-constructs.ThronEndpointApiGatewayProps.property.apiGatewayApi"></a>

```go
ApiGatewayApi IRestApi
```

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_apigateway.IRestApi

The API on which the endpoint should be added.

---

##### `BasePath`<sup>Required</sup> <a name="BasePath" id="cdk-constructs.ThronEndpointApiGatewayProps.property.basePath"></a>

```go
BasePath *string
```

- *Type:* *string

The path on which to add the endpoint.

---

##### `LambdaFunction`<sup>Required</sup> <a name="LambdaFunction" id="cdk-constructs.ThronEndpointApiGatewayProps.property.lambdaFunction"></a>

```go
LambdaFunction IFunction
```

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_lambda.IFunction

The function to attach to the endpoint.

---

##### `Timeout`<sup>Required</sup> <a name="Timeout" id="cdk-constructs.ThronEndpointApiGatewayProps.property.timeout"></a>

```go
Timeout Duration
```

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.Duration

The timeout of the integration.

---

### ThronHealthCheckOverride <a name="ThronHealthCheckOverride" id="cdk-constructs.ThronHealthCheckOverride"></a>

#### Initializer <a name="Initializer" id="cdk-constructs.ThronHealthCheckOverride.Initializer"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

&cdkconstructs.ThronHealthCheckOverride {
	HealthyHttpCodes: *string,
	HealthyThresholdCount: *f64,
	Interval: github.com/aws/aws-cdk-go/awscdk/v2.Duration,
	Path: *string,
	Port: *string,
	Timeout: github.com/aws/aws-cdk-go/awscdk/v2.Duration,
	UnhealthyThresholdCount: *f64,
}
```

#### Properties <a name="Properties" id="Properties"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.ThronHealthCheckOverride.property.healthyHttpCodes">HealthyHttpCodes</a></code> | <code>*string</code> | *No description.* |
| <code><a href="#cdk-constructs.ThronHealthCheckOverride.property.healthyThresholdCount">HealthyThresholdCount</a></code> | <code>*f64</code> | *No description.* |
| <code><a href="#cdk-constructs.ThronHealthCheckOverride.property.interval">Interval</a></code> | <code>github.com/aws/aws-cdk-go/awscdk/v2.Duration</code> | *No description.* |
| <code><a href="#cdk-constructs.ThronHealthCheckOverride.property.path">Path</a></code> | <code>*string</code> | *No description.* |
| <code><a href="#cdk-constructs.ThronHealthCheckOverride.property.port">Port</a></code> | <code>*string</code> | *No description.* |
| <code><a href="#cdk-constructs.ThronHealthCheckOverride.property.timeout">Timeout</a></code> | <code>github.com/aws/aws-cdk-go/awscdk/v2.Duration</code> | *No description.* |
| <code><a href="#cdk-constructs.ThronHealthCheckOverride.property.unhealthyThresholdCount">UnhealthyThresholdCount</a></code> | <code>*f64</code> | *No description.* |

---

##### `HealthyHttpCodes`<sup>Optional</sup> <a name="HealthyHttpCodes" id="cdk-constructs.ThronHealthCheckOverride.property.healthyHttpCodes"></a>

```go
HealthyHttpCodes *string
```

- *Type:* *string

---

##### `HealthyThresholdCount`<sup>Optional</sup> <a name="HealthyThresholdCount" id="cdk-constructs.ThronHealthCheckOverride.property.healthyThresholdCount"></a>

```go
HealthyThresholdCount *f64
```

- *Type:* *f64

---

##### `Interval`<sup>Optional</sup> <a name="Interval" id="cdk-constructs.ThronHealthCheckOverride.property.interval"></a>

```go
Interval Duration
```

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.Duration

---

##### `Path`<sup>Optional</sup> <a name="Path" id="cdk-constructs.ThronHealthCheckOverride.property.path"></a>

```go
Path *string
```

- *Type:* *string

---

##### `Port`<sup>Optional</sup> <a name="Port" id="cdk-constructs.ThronHealthCheckOverride.property.port"></a>

```go
Port *string
```

- *Type:* *string

---

##### `Timeout`<sup>Optional</sup> <a name="Timeout" id="cdk-constructs.ThronHealthCheckOverride.property.timeout"></a>

```go
Timeout Duration
```

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.Duration

---

##### `UnhealthyThresholdCount`<sup>Optional</sup> <a name="UnhealthyThresholdCount" id="cdk-constructs.ThronHealthCheckOverride.property.unhealthyThresholdCount"></a>

```go
UnhealthyThresholdCount *f64
```

- *Type:* *f64

---

### ThronLambdaApiGatewayEndpointProps <a name="ThronLambdaApiGatewayEndpointProps" id="cdk-constructs.ThronLambdaApiGatewayEndpointProps"></a>

#### Initializer <a name="Initializer" id="cdk-constructs.ThronLambdaApiGatewayEndpointProps.Initializer"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

&cdkconstructs.ThronLambdaApiGatewayEndpointProps {
	ServiceGroup: git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs.ServiceGroup,
	Version: *f64,
	Visibility: git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs.EndpointVisibility,
	ServiceName: *string,
	ApiGatewayOverride: git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs.ThronApiGatewayApi,
	PathOverride: *string,
}
```

#### Properties <a name="Properties" id="Properties"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.ThronLambdaApiGatewayEndpointProps.property.serviceGroup">ServiceGroup</a></code> | <code><a href="#cdk-constructs.ServiceGroup">ServiceGroup</a></code> | Service group of the service. |
| <code><a href="#cdk-constructs.ThronLambdaApiGatewayEndpointProps.property.version">Version</a></code> | <code>*f64</code> | The version of the API exposed by the endpoint. |
| <code><a href="#cdk-constructs.ThronLambdaApiGatewayEndpointProps.property.visibility">Visibility</a></code> | <code><a href="#cdk-constructs.EndpointVisibility">EndpointVisibility</a></code> | Wether the endpoint is private or public. |
| <code><a href="#cdk-constructs.ThronLambdaApiGatewayEndpointProps.property.serviceName">ServiceName</a></code> | <code>*string</code> | Name of the service the endpoint exposes. |
| <code><a href="#cdk-constructs.ThronLambdaApiGatewayEndpointProps.property.apiGatewayOverride">ApiGatewayOverride</a></code> | <code><a href="#cdk-constructs.ThronApiGatewayApi">ThronApiGatewayApi</a></code> | If this params is provided, no new Api Gateway will be created. |
| <code><a href="#cdk-constructs.ThronLambdaApiGatewayEndpointProps.property.pathOverride">PathOverride</a></code> | <code>*string</code> | If this params is provided, the path of the service will be overridden with the given one. |

---

##### `ServiceGroup`<sup>Optional</sup> <a name="ServiceGroup" id="cdk-constructs.ThronLambdaApiGatewayEndpointProps.property.serviceGroup"></a>

```go
ServiceGroup ServiceGroup
```

- *Type:* <a href="#cdk-constructs.ServiceGroup">ServiceGroup</a>
- *Default:* ServiceGroup.VIEW

Service group of the service.

---

##### `Version`<sup>Optional</sup> <a name="Version" id="cdk-constructs.ThronLambdaApiGatewayEndpointProps.property.version"></a>

```go
Version *f64
```

- *Type:* *f64
- *Default:* 1

The version of the API exposed by the endpoint.

---

##### `Visibility`<sup>Optional</sup> <a name="Visibility" id="cdk-constructs.ThronLambdaApiGatewayEndpointProps.property.visibility"></a>

```go
Visibility EndpointVisibility
```

- *Type:* <a href="#cdk-constructs.EndpointVisibility">EndpointVisibility</a>
- *Default:* EndpointVisibility.PRIVATE

Wether the endpoint is private or public.

---

##### `ServiceName`<sup>Required</sup> <a name="ServiceName" id="cdk-constructs.ThronLambdaApiGatewayEndpointProps.property.serviceName"></a>

```go
ServiceName *string
```

- *Type:* *string

Name of the service the endpoint exposes.

---

##### `ApiGatewayOverride`<sup>Optional</sup> <a name="ApiGatewayOverride" id="cdk-constructs.ThronLambdaApiGatewayEndpointProps.property.apiGatewayOverride"></a>

```go
ApiGatewayOverride ThronApiGatewayApi
```

- *Type:* <a href="#cdk-constructs.ThronApiGatewayApi">ThronApiGatewayApi</a>

If this params is provided, no new Api Gateway will be created.

Instead, the provided api gateway will be used

---

##### `PathOverride`<sup>Optional</sup> <a name="PathOverride" id="cdk-constructs.ThronLambdaApiGatewayEndpointProps.property.pathOverride"></a>

```go
PathOverride *string
```

- *Type:* *string

If this params is provided, the path of the service will be overridden with the given one.

---

### ThronLambdaMicroservicePipelineProps <a name="ThronLambdaMicroservicePipelineProps" id="cdk-constructs.ThronLambdaMicroservicePipelineProps"></a>

ThronLambdaMicroservicePipeline Props.

#### Initializer <a name="Initializer" id="cdk-constructs.ThronLambdaMicroservicePipelineProps.Initializer"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

&cdkconstructs.ThronLambdaMicroservicePipelineProps {
	CicdConfig: *map[string]git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs.CicdEnvironment,
	CustomBuildImage: github.com/aws/aws-cdk-go/awscdk/v2.aws_codebuild.IBuildImage,
	Lambdas: *map[string]git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs.StepConfig,
	ProjectId: *string,
	Tests: *map[string]git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs.StepConfig,
	PreExistingArtifactBucket: *string,
	PreExistingRepositoryName: *string,
	ProjectPreset: git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs.ProjectPreset,
}
```

#### Properties <a name="Properties" id="Properties"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.ThronLambdaMicroservicePipelineProps.property.cicdConfig">CicdConfig</a></code> | <code>*map[string]<a href="#cdk-constructs.CicdEnvironment">CicdEnvironment</a></code> | Target accounts for pipeline and other CICD settings. |
| <code><a href="#cdk-constructs.ThronLambdaMicroservicePipelineProps.property.customBuildImage">CustomBuildImage</a></code> | <code>github.com/aws/aws-cdk-go/awscdk/v2.aws_codebuild.IBuildImage</code> | Build Image to be used by default in all the lambda steps. |
| <code><a href="#cdk-constructs.ThronLambdaMicroservicePipelineProps.property.lambdas">Lambdas</a></code> | <code>*map[string]<a href="#cdk-constructs.StepConfig">StepConfig</a></code> | Map of all the lambdas id along with their {@link StepConfiguration}. |
| <code><a href="#cdk-constructs.ThronLambdaMicroservicePipelineProps.property.projectId">ProjectId</a></code> | <code>*string</code> | Id of the applicative project to use. |
| <code><a href="#cdk-constructs.ThronLambdaMicroservicePipelineProps.property.tests">Tests</a></code> | <code>*map[string]<a href="#cdk-constructs.StepConfig">StepConfig</a></code> | Map of all the tests id along with their {@link StepConfiguration}. |
| <code><a href="#cdk-constructs.ThronLambdaMicroservicePipelineProps.property.preExistingArtifactBucket">PreExistingArtifactBucket</a></code> | <code>*string</code> | If specified, uses an existing bucket for storing artifacts. |
| <code><a href="#cdk-constructs.ThronLambdaMicroservicePipelineProps.property.preExistingRepositoryName">PreExistingRepositoryName</a></code> | <code>*string</code> | If specified, define a source codecommit repository instead of creating one. |
| <code><a href="#cdk-constructs.ThronLambdaMicroservicePipelineProps.property.projectPreset">ProjectPreset</a></code> | <code><a href="#cdk-constructs.ProjectPreset">ProjectPreset</a></code> | If specified, the new project will be initialized with the chosen codebase, after the subs have been performed Note: You cannot specify this attribute if `preExistingRepositoryName` is specified. |

---

##### `CicdConfig`<sup>Required</sup> <a name="CicdConfig" id="cdk-constructs.ThronLambdaMicroservicePipelineProps.property.cicdConfig"></a>

```go
CicdConfig *map[string]CicdEnvironment
```

- *Type:* *map[string]<a href="#cdk-constructs.CicdEnvironment">CicdEnvironment</a>

Target accounts for pipeline and other CICD settings.

---

##### `CustomBuildImage`<sup>Required</sup> <a name="CustomBuildImage" id="cdk-constructs.ThronLambdaMicroservicePipelineProps.property.customBuildImage"></a>

```go
CustomBuildImage IBuildImage
```

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_codebuild.IBuildImage

Build Image to be used by default in all the lambda steps.

---

##### `Lambdas`<sup>Required</sup> <a name="Lambdas" id="cdk-constructs.ThronLambdaMicroservicePipelineProps.property.lambdas"></a>

```go
Lambdas *map[string]StepConfig
```

- *Type:* *map[string]<a href="#cdk-constructs.StepConfig">StepConfig</a>

Map of all the lambdas id along with their {@link StepConfiguration}.

Lambdas ids must:

* Be between 3 and 25 longs and only letters
* Not be repeated (case insensitive).

---

##### `ProjectId`<sup>Required</sup> <a name="ProjectId" id="cdk-constructs.ThronLambdaMicroservicePipelineProps.property.projectId"></a>

```go
ProjectId *string
```

- *Type:* *string

Id of the applicative project to use.

If the app project is `products-sync`, projectId should be `product-sync`. Resources prefixes will automatically append `-cicd-{env}`
after the prefix. In the aforementioned example, all the resources will be prefixed with `product-sync-cicd-development`, `product-sync-cicd-quality` or `product-sync-cicd-production`
based on the environment

---

##### `Tests`<sup>Required</sup> <a name="Tests" id="cdk-constructs.ThronLambdaMicroservicePipelineProps.property.tests"></a>

```go
Tests *map[string]StepConfig
```

- *Type:* *map[string]<a href="#cdk-constructs.StepConfig">StepConfig</a>

Map of all the tests id along with their {@link StepConfiguration}.

Test ids must:

* Be between 3 and 25 longs and only letters
* Not be repeated (case insensitive).

---

##### `PreExistingArtifactBucket`<sup>Optional</sup> <a name="PreExistingArtifactBucket" id="cdk-constructs.ThronLambdaMicroservicePipelineProps.property.preExistingArtifactBucket"></a>

```go
PreExistingArtifactBucket *string
```

- *Type:* *string

If specified, uses an existing bucket for storing artifacts.

---

##### `PreExistingRepositoryName`<sup>Optional</sup> <a name="PreExistingRepositoryName" id="cdk-constructs.ThronLambdaMicroservicePipelineProps.property.preExistingRepositoryName"></a>

```go
PreExistingRepositoryName *string
```

- *Type:* *string

If specified, define a source codecommit repository instead of creating one.

Note: You cannot specify this attribute if `projectPreset` is specified

---

##### `ProjectPreset`<sup>Optional</sup> <a name="ProjectPreset" id="cdk-constructs.ThronLambdaMicroservicePipelineProps.property.projectPreset"></a>

```go
ProjectPreset ProjectPreset
```

- *Type:* <a href="#cdk-constructs.ProjectPreset">ProjectPreset</a>

If specified, the new project will be initialized with the chosen codebase, after the subs have been performed Note: You cannot specify this attribute if `preExistingRepositoryName` is specified.

---

*Example*

```go
// Example automatically generated from non-compiling source. May contain errors.
{repositoryBranchTagOrSha: "master",
	     repositoryName"golang-project-template" , repositoryRegion"eu-west-1" , subConfigs[]map[string]*string{
		map[string]*string{
			"searchValue": jsii.String("##project-name##"),
			"replaceValue": jsii.String("sample-project-id }"),
		},
	}
}
```


### ThronLambdaSingleEnvPipelineCodeCommitProps <a name="ThronLambdaSingleEnvPipelineCodeCommitProps" id="cdk-constructs.ThronLambdaSingleEnvPipelineCodeCommitProps"></a>

Codecommit configuration for the Source Phase of the pipeline.

#### Initializer <a name="Initializer" id="cdk-constructs.ThronLambdaSingleEnvPipelineCodeCommitProps.Initializer"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

&cdkconstructs.ThronLambdaSingleEnvPipelineCodeCommitProps {
	Branch: *string,
	Repository: github.com/aws/aws-cdk-go/awscdk/v2.aws_codecommit.IRepository,
}
```

#### Properties <a name="Properties" id="Properties"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.ThronLambdaSingleEnvPipelineCodeCommitProps.property.branch">Branch</a></code> | <code>*string</code> | Repository branch on which the pipeline trigger is set. |
| <code><a href="#cdk-constructs.ThronLambdaSingleEnvPipelineCodeCommitProps.property.repository">Repository</a></code> | <code>github.com/aws/aws-cdk-go/awscdk/v2.aws_codecommit.IRepository</code> | Repository on which the pipeline trigger is set. |

---

##### `Branch`<sup>Required</sup> <a name="Branch" id="cdk-constructs.ThronLambdaSingleEnvPipelineCodeCommitProps.property.branch"></a>

```go
Branch *string
```

- *Type:* *string

Repository branch on which the pipeline trigger is set.

---

##### `Repository`<sup>Required</sup> <a name="Repository" id="cdk-constructs.ThronLambdaSingleEnvPipelineCodeCommitProps.property.repository"></a>

```go
Repository IRepository
```

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_codecommit.IRepository

Repository on which the pipeline trigger is set.

---

### ThronLambdaSingleEnvPipelineProps <a name="ThronLambdaSingleEnvPipelineProps" id="cdk-constructs.ThronLambdaSingleEnvPipelineProps"></a>

ThronLambdaSingleEnvPipeline Props.

#### Initializer <a name="Initializer" id="cdk-constructs.ThronLambdaSingleEnvPipelineProps.Initializer"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

&cdkconstructs.ThronLambdaSingleEnvPipelineProps {
	ArtifactBucket: github.com/aws/aws-cdk-go/awscdk/v2.aws_s3.IBucket,
	CodeCommitConfig: git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs.ThronLambdaSingleEnvPipelineCodeCommitProps,
	DeployConf: git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs.DeployStepConf,
	LambdasConf: *map[string]git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs.LambdaConf,
	Prefix: *string,
	TestConf: *map[string]git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs.StepConfig,
	IsBuildEnabled: *bool,
	NotifyConf: git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs.NotifyConf,
}
```

#### Properties <a name="Properties" id="Properties"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.ThronLambdaSingleEnvPipelineProps.property.artifactBucket">ArtifactBucket</a></code> | <code>github.com/aws/aws-cdk-go/awscdk/v2.aws_s3.IBucket</code> | The bucket to store the artifacts. |
| <code><a href="#cdk-constructs.ThronLambdaSingleEnvPipelineProps.property.codeCommitConfig">CodeCommitConfig</a></code> | <code><a href="#cdk-constructs.ThronLambdaSingleEnvPipelineCodeCommitProps">ThronLambdaSingleEnvPipelineCodeCommitProps</a></code> | The configuration for the code commit repository. |
| <code><a href="#cdk-constructs.ThronLambdaSingleEnvPipelineProps.property.deployConf">DeployConf</a></code> | <code><a href="#cdk-constructs.DeployStepConf">DeployStepConf</a></code> | The Configuration for the Deploy Step. |
| <code><a href="#cdk-constructs.ThronLambdaSingleEnvPipelineProps.property.lambdasConf">LambdasConf</a></code> | <code>*map[string]<a href="#cdk-constructs.LambdaConf">LambdaConf</a></code> | Lambda Configurations. |
| <code><a href="#cdk-constructs.ThronLambdaSingleEnvPipelineProps.property.prefix">Prefix</a></code> | <code>*string</code> | Prefix for resources. |
| <code><a href="#cdk-constructs.ThronLambdaSingleEnvPipelineProps.property.testConf">TestConf</a></code> | <code>*map[string]<a href="#cdk-constructs.StepConfig">StepConfig</a></code> | The ids of the tests to run. |
| <code><a href="#cdk-constructs.ThronLambdaSingleEnvPipelineProps.property.isBuildEnabled">IsBuildEnabled</a></code> | <code>*bool</code> | Whether or not the build stage is enabled. |
| <code><a href="#cdk-constructs.ThronLambdaSingleEnvPipelineProps.property.notifyConf">NotifyConf</a></code> | <code><a href="#cdk-constructs.NotifyConf">NotifyConf</a></code> | Configuration for enabling pipeline notifications. |

---

##### `ArtifactBucket`<sup>Required</sup> <a name="ArtifactBucket" id="cdk-constructs.ThronLambdaSingleEnvPipelineProps.property.artifactBucket"></a>

```go
ArtifactBucket IBucket
```

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_s3.IBucket

The bucket to store the artifacts.

---

##### `CodeCommitConfig`<sup>Required</sup> <a name="CodeCommitConfig" id="cdk-constructs.ThronLambdaSingleEnvPipelineProps.property.codeCommitConfig"></a>

```go
CodeCommitConfig ThronLambdaSingleEnvPipelineCodeCommitProps
```

- *Type:* <a href="#cdk-constructs.ThronLambdaSingleEnvPipelineCodeCommitProps">ThronLambdaSingleEnvPipelineCodeCommitProps</a>

The configuration for the code commit repository.

---

##### `DeployConf`<sup>Required</sup> <a name="DeployConf" id="cdk-constructs.ThronLambdaSingleEnvPipelineProps.property.deployConf"></a>

```go
DeployConf DeployStepConf
```

- *Type:* <a href="#cdk-constructs.DeployStepConf">DeployStepConf</a>

The Configuration for the Deploy Step.

---

##### `LambdasConf`<sup>Required</sup> <a name="LambdasConf" id="cdk-constructs.ThronLambdaSingleEnvPipelineProps.property.lambdasConf"></a>

```go
LambdasConf *map[string]LambdaConf
```

- *Type:* *map[string]<a href="#cdk-constructs.LambdaConf">LambdaConf</a>

Lambda Configurations.

---

##### `Prefix`<sup>Required</sup> <a name="Prefix" id="cdk-constructs.ThronLambdaSingleEnvPipelineProps.property.prefix"></a>

```go
Prefix *string
```

- *Type:* *string

Prefix for resources.

---

##### `TestConf`<sup>Required</sup> <a name="TestConf" id="cdk-constructs.ThronLambdaSingleEnvPipelineProps.property.testConf"></a>

```go
TestConf *map[string]StepConfig
```

- *Type:* *map[string]<a href="#cdk-constructs.StepConfig">StepConfig</a>

The ids of the tests to run.

---

##### `IsBuildEnabled`<sup>Optional</sup> <a name="IsBuildEnabled" id="cdk-constructs.ThronLambdaSingleEnvPipelineProps.property.isBuildEnabled"></a>

```go
IsBuildEnabled *bool
```

- *Type:* *bool

Whether or not the build stage is enabled.

Defaults to true

---

##### `NotifyConf`<sup>Optional</sup> <a name="NotifyConf" id="cdk-constructs.ThronLambdaSingleEnvPipelineProps.property.notifyConf"></a>

```go
NotifyConf NotifyConf
```

- *Type:* <a href="#cdk-constructs.NotifyConf">NotifyConf</a>

Configuration for enabling pipeline notifications.

---

### ThronNewRelicContextInjectorOptions <a name="ThronNewRelicContextInjectorOptions" id="cdk-constructs.ThronNewRelicContextInjectorOptions"></a>

#### Initializer <a name="Initializer" id="cdk-constructs.ThronNewRelicContextInjectorOptions.Initializer"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

&cdkconstructs.ThronNewRelicContextInjectorOptions {
	NewRelicConfigOverrides: git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs.NewRelicLambdaConfigOverrides,
}
```

#### Properties <a name="Properties" id="Properties"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.ThronNewRelicContextInjectorOptions.property.newRelicConfigOverrides">NewRelicConfigOverrides</a></code> | <code><a href="#cdk-constructs.NewRelicLambdaConfigOverrides">NewRelicLambdaConfigOverrides</a></code> | Explicit Overrides for NewRelic Configuration. |

---

##### `NewRelicConfigOverrides`<sup>Optional</sup> <a name="NewRelicConfigOverrides" id="cdk-constructs.ThronNewRelicContextInjectorOptions.property.newRelicConfigOverrides"></a>

```go
NewRelicConfigOverrides NewRelicLambdaConfigOverrides
```

- *Type:* <a href="#cdk-constructs.NewRelicLambdaConfigOverrides">NewRelicLambdaConfigOverrides</a>
- *Default:* Empty object with no overrides

Explicit Overrides for NewRelic Configuration.

---

### ThronPipelineBuildProjectProps <a name="ThronPipelineBuildProjectProps" id="cdk-constructs.ThronPipelineBuildProjectProps"></a>

#### Initializer <a name="Initializer" id="cdk-constructs.ThronPipelineBuildProjectProps.Initializer"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

&cdkconstructs.ThronPipelineBuildProjectProps {
	BuildName: *string,
	ProjectPrefix: *string,
	BuildImage: github.com/aws/aws-cdk-go/awscdk/v2.aws_codebuild.IBuildImage,
	BuildSpecPath: *string,
	ComputeType: github.com/aws/aws-cdk-go/awscdk/v2.aws_codebuild.ComputeType,
	EnvironmentalVariables: *map[string]github.com/aws/aws-cdk-go/awscdk/v2.aws_codebuild.BuildEnvironmentVariable,
}
```

#### Properties <a name="Properties" id="Properties"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.ThronPipelineBuildProjectProps.property.buildName">BuildName</a></code> | <code>*string</code> | *No description.* |
| <code><a href="#cdk-constructs.ThronPipelineBuildProjectProps.property.projectPrefix">ProjectPrefix</a></code> | <code>*string</code> | *No description.* |
| <code><a href="#cdk-constructs.ThronPipelineBuildProjectProps.property.buildImage">BuildImage</a></code> | <code>github.com/aws/aws-cdk-go/awscdk/v2.aws_codebuild.IBuildImage</code> | *No description.* |
| <code><a href="#cdk-constructs.ThronPipelineBuildProjectProps.property.buildSpecPath">BuildSpecPath</a></code> | <code>*string</code> | *No description.* |
| <code><a href="#cdk-constructs.ThronPipelineBuildProjectProps.property.computeType">ComputeType</a></code> | <code>github.com/aws/aws-cdk-go/awscdk/v2.aws_codebuild.ComputeType</code> | *No description.* |
| <code><a href="#cdk-constructs.ThronPipelineBuildProjectProps.property.environmentalVariables">EnvironmentalVariables</a></code> | <code>*map[string]github.com/aws/aws-cdk-go/awscdk/v2.aws_codebuild.BuildEnvironmentVariable</code> | *No description.* |

---

##### `BuildName`<sup>Required</sup> <a name="BuildName" id="cdk-constructs.ThronPipelineBuildProjectProps.property.buildName"></a>

```go
BuildName *string
```

- *Type:* *string

---

##### `ProjectPrefix`<sup>Required</sup> <a name="ProjectPrefix" id="cdk-constructs.ThronPipelineBuildProjectProps.property.projectPrefix"></a>

```go
ProjectPrefix *string
```

- *Type:* *string

---

##### `BuildImage`<sup>Optional</sup> <a name="BuildImage" id="cdk-constructs.ThronPipelineBuildProjectProps.property.buildImage"></a>

```go
BuildImage IBuildImage
```

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_codebuild.IBuildImage

---

##### `BuildSpecPath`<sup>Optional</sup> <a name="BuildSpecPath" id="cdk-constructs.ThronPipelineBuildProjectProps.property.buildSpecPath"></a>

```go
BuildSpecPath *string
```

- *Type:* *string

---

##### `ComputeType`<sup>Optional</sup> <a name="ComputeType" id="cdk-constructs.ThronPipelineBuildProjectProps.property.computeType"></a>

```go
ComputeType ComputeType
```

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_codebuild.ComputeType

---

##### `EnvironmentalVariables`<sup>Optional</sup> <a name="EnvironmentalVariables" id="cdk-constructs.ThronPipelineBuildProjectProps.property.environmentalVariables"></a>

```go
EnvironmentalVariables *map[string]BuildEnvironmentVariable
```

- *Type:* *map[string]github.com/aws/aws-cdk-go/awscdk/v2.aws_codebuild.BuildEnvironmentVariable

---

### ThronResponseHeaderPolicyProps <a name="ThronResponseHeaderPolicyProps" id="cdk-constructs.ThronResponseHeaderPolicyProps"></a>

#### Initializer <a name="Initializer" id="cdk-constructs.ThronResponseHeaderPolicyProps.Initializer"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

&cdkconstructs.ThronResponseHeaderPolicyProps {
	AdditionalCustomHeaders: *[]github.com/aws/aws-cdk-go/awscdk/v2.aws_cloudfront.ResponseCustomHeader,
	Csp: *string,
}
```

#### Properties <a name="Properties" id="Properties"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.ThronResponseHeaderPolicyProps.property.additionalCustomHeaders">AdditionalCustomHeaders</a></code> | <code>*[]github.com/aws/aws-cdk-go/awscdk/v2.aws_cloudfront.ResponseCustomHeader</code> | *No description.* |
| <code><a href="#cdk-constructs.ThronResponseHeaderPolicyProps.property.csp">Csp</a></code> | <code>*string</code> | Content Security Policy header to set. |

---

##### `AdditionalCustomHeaders`<sup>Optional</sup> <a name="AdditionalCustomHeaders" id="cdk-constructs.ThronResponseHeaderPolicyProps.property.additionalCustomHeaders"></a>

```go
AdditionalCustomHeaders *[]ResponseCustomHeader
```

- *Type:* *[]github.com/aws/aws-cdk-go/awscdk/v2.aws_cloudfront.ResponseCustomHeader

---

##### `Csp`<sup>Optional</sup> <a name="Csp" id="cdk-constructs.ThronResponseHeaderPolicyProps.property.csp"></a>

```go
Csp *string
```

- *Type:* *string

Content Security Policy header to set.

---

### ThronTargetScalingProps <a name="ThronTargetScalingProps" id="cdk-constructs.ThronTargetScalingProps"></a>

#### Initializer <a name="Initializer" id="cdk-constructs.ThronTargetScalingProps.Initializer"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

&cdkconstructs.ThronTargetScalingProps {
	MaxCapacity: *f64,
	MinCapacity: *f64,
	TargetValue: *f64,
	PredefinedMetric: github.com/aws/aws-cdk-go/awscdk/v2.aws_applicationautoscaling.PredefinedMetric,
	ScaleInCooldown: github.com/aws/aws-cdk-go/awscdk/v2.Duration,
	ScaleOutCooldown: github.com/aws/aws-cdk-go/awscdk/v2.Duration,
}
```

#### Properties <a name="Properties" id="Properties"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.ThronTargetScalingProps.property.maxCapacity">MaxCapacity</a></code> | <code>*f64</code> | The maximum value that Application Auto Scaling can use to scale a target during a scaling activity. |
| <code><a href="#cdk-constructs.ThronTargetScalingProps.property.minCapacity">MinCapacity</a></code> | <code>*f64</code> | The minimum value that Application Auto Scaling can use to scale a target during a scaling activity. |
| <code><a href="#cdk-constructs.ThronTargetScalingProps.property.targetValue">TargetValue</a></code> | <code>*f64</code> | The target value for the metric. |
| <code><a href="#cdk-constructs.ThronTargetScalingProps.property.predefinedMetric">PredefinedMetric</a></code> | <code>github.com/aws/aws-cdk-go/awscdk/v2.aws_applicationautoscaling.PredefinedMetric</code> | A predefined metric for application autoscaling. |
| <code><a href="#cdk-constructs.ThronTargetScalingProps.property.scaleInCooldown">ScaleInCooldown</a></code> | <code>github.com/aws/aws-cdk-go/awscdk/v2.Duration</code> | The amount of time after a scale in activity completes before another scale in activity can start. |
| <code><a href="#cdk-constructs.ThronTargetScalingProps.property.scaleOutCooldown">ScaleOutCooldown</a></code> | <code>github.com/aws/aws-cdk-go/awscdk/v2.Duration</code> | The amount of time after a scale in activity completes before another scale in activity can start. |

---

##### `MaxCapacity`<sup>Required</sup> <a name="MaxCapacity" id="cdk-constructs.ThronTargetScalingProps.property.maxCapacity"></a>

```go
MaxCapacity *f64
```

- *Type:* *f64

The maximum value that Application Auto Scaling can use to scale a target during a scaling activity.

---

##### `MinCapacity`<sup>Required</sup> <a name="MinCapacity" id="cdk-constructs.ThronTargetScalingProps.property.minCapacity"></a>

```go
MinCapacity *f64
```

- *Type:* *f64

The minimum value that Application Auto Scaling can use to scale a target during a scaling activity.

---

##### `TargetValue`<sup>Required</sup> <a name="TargetValue" id="cdk-constructs.ThronTargetScalingProps.property.targetValue"></a>

```go
TargetValue *f64
```

- *Type:* *f64

The target value for the metric.

---

##### `PredefinedMetric`<sup>Optional</sup> <a name="PredefinedMetric" id="cdk-constructs.ThronTargetScalingProps.property.predefinedMetric"></a>

```go
PredefinedMetric PredefinedMetric
```

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_applicationautoscaling.PredefinedMetric

A predefined metric for application autoscaling.

The metric must track utilization. Scaling out will happen if the metric is higher than the target value,
scaling in will happen in the metric is lower than the target value.

---

##### `ScaleInCooldown`<sup>Optional</sup> <a name="ScaleInCooldown" id="cdk-constructs.ThronTargetScalingProps.property.scaleInCooldown"></a>

```go
ScaleInCooldown Duration
```

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.Duration
- *Default:* Duration.minutes(300)

The amount of time after a scale in activity completes before another scale in activity can start.

---

##### `ScaleOutCooldown`<sup>Optional</sup> <a name="ScaleOutCooldown" id="cdk-constructs.ThronTargetScalingProps.property.scaleOutCooldown"></a>

```go
ScaleOutCooldown Duration
```

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.Duration
- *Default:* Duration.minutes(90)

The amount of time after a scale in activity completes before another scale in activity can start.

---

### ThronVpcProps <a name="ThronVpcProps" id="cdk-constructs.ThronVpcProps"></a>

ThronVPC Props.

#### Initializer <a name="Initializer" id="cdk-constructs.ThronVpcProps.Initializer"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

&cdkconstructs.ThronVpcProps {
	GatewayEndpoints: *[]github.com/aws/aws-cdk-go/awscdk/v2.aws_ec2.GatewayVpcEndpointAwsService,
	InterfaceEndpoints: *[]github.com/aws/aws-cdk-go/awscdk/v2.aws_ec2.InterfaceVpcEndpointAwsService,
	Ipv4Cidr: *string,
	IsNatHA: *bool,
	Prefix: *string,
	SubnetsConfigs: *[]git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs.SubnetConfigProps,
}
```

#### Properties <a name="Properties" id="Properties"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.ThronVpcProps.property.gatewayEndpoints">GatewayEndpoints</a></code> | <code>*[]github.com/aws/aws-cdk-go/awscdk/v2.aws_ec2.GatewayVpcEndpointAwsService</code> | Set of gateway endpoints to use in the VPC. |
| <code><a href="#cdk-constructs.ThronVpcProps.property.interfaceEndpoints">InterfaceEndpoints</a></code> | <code>*[]github.com/aws/aws-cdk-go/awscdk/v2.aws_ec2.InterfaceVpcEndpointAwsService</code> | Set of interface Endpoints to add to the VPC. |
| <code><a href="#cdk-constructs.ThronVpcProps.property.ipv4Cidr">Ipv4Cidr</a></code> | <code>*string</code> | IPv4 CIDR to assign to the VPC. |
| <code><a href="#cdk-constructs.ThronVpcProps.property.isNatHA">IsNatHA</a></code> | <code>*bool</code> | Whether to use a High Availability NAT configuration. |
| <code><a href="#cdk-constructs.ThronVpcProps.property.prefix">Prefix</a></code> | <code>*string</code> | Prefix to name all the child resources with. |
| <code><a href="#cdk-constructs.ThronVpcProps.property.subnetsConfigs">SubnetsConfigs</a></code> | <code>*[]<a href="#cdk-constructs.SubnetConfigProps">SubnetConfigProps</a></code> | Subnet configurations for the VPC. |

---

##### `GatewayEndpoints`<sup>Required</sup> <a name="GatewayEndpoints" id="cdk-constructs.ThronVpcProps.property.gatewayEndpoints"></a>

```go
GatewayEndpoints *[]GatewayVpcEndpointAwsService
```

- *Type:* *[]github.com/aws/aws-cdk-go/awscdk/v2.aws_ec2.GatewayVpcEndpointAwsService

Set of gateway endpoints to use in the VPC.

As they are free, put them all by default! (DYNAMO + S3)

---

##### `InterfaceEndpoints`<sup>Required</sup> <a name="InterfaceEndpoints" id="cdk-constructs.ThronVpcProps.property.interfaceEndpoints"></a>

```go
InterfaceEndpoints *[]InterfaceVpcEndpointAwsService
```

- *Type:* *[]github.com/aws/aws-cdk-go/awscdk/v2.aws_ec2.InterfaceVpcEndpointAwsService

Set of interface Endpoints to add to the VPC.

---

##### `Ipv4Cidr`<sup>Required</sup> <a name="Ipv4Cidr" id="cdk-constructs.ThronVpcProps.property.ipv4Cidr"></a>

```go
Ipv4Cidr *string
```

- *Type:* *string

IPv4 CIDR to assign to the VPC.

---

##### `IsNatHA`<sup>Required</sup> <a name="IsNatHA" id="cdk-constructs.ThronVpcProps.property.isNatHA"></a>

```go
IsNatHA *bool
```

- *Type:* *bool

Whether to use a High Availability NAT configuration.

If `true` a NAT will be created in each public subnet, and each private subnets' default route will point to its corresponding az NAT

If `false` a NAT will be created only in the first (alphabetically speaking) zone, and each private subnets' default route will point to it

---

##### `Prefix`<sup>Required</sup> <a name="Prefix" id="cdk-constructs.ThronVpcProps.property.prefix"></a>

```go
Prefix *string
```

- *Type:* *string

Prefix to name all the child resources with.

---

##### `SubnetsConfigs`<sup>Required</sup> <a name="SubnetsConfigs" id="cdk-constructs.ThronVpcProps.property.subnetsConfigs"></a>

```go
SubnetsConfigs *[]SubnetConfigProps
```

- *Type:* *[]<a href="#cdk-constructs.SubnetConfigProps">SubnetConfigProps</a>

Subnet configurations for the VPC.

---

## Classes <a name="Classes" id="Classes"></a>

### DockerImageName <a name="DockerImageName" id="cdk-constructs.DockerImageName"></a>

- *Implements:* <a href="#cdk-constructs.IImageName">IImageName</a>

#### Initializers <a name="Initializers" id="cdk-constructs.DockerImageName.Initializer"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

cdkconstructs.NewDockerImageName(name *string, creds *string) DockerImageName
```

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.DockerImageName.Initializer.parameter.name">name</a></code> | <code>*string</code> | *No description.* |
| <code><a href="#cdk-constructs.DockerImageName.Initializer.parameter.creds">creds</a></code> | <code>*string</code> | The credentials of the docker image. |

---

##### `name`<sup>Required</sup> <a name="name" id="cdk-constructs.DockerImageName.Initializer.parameter.name"></a>

- *Type:* *string

---

##### `creds`<sup>Optional</sup> <a name="creds" id="cdk-constructs.DockerImageName.Initializer.parameter.creds"></a>

- *Type:* *string

The credentials of the docker image.

Format `user:password` or `AWS Secrets Manager secret arn` or `AWS Secrets Manager secret name`

---



#### Properties <a name="Properties" id="Properties"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.DockerImageName.property.uri">Uri</a></code> | <code>*string</code> | The uri of the docker image. |
| <code><a href="#cdk-constructs.DockerImageName.property.creds">Creds</a></code> | <code>*string</code> | The credentials of the docker image. |

---

##### `Uri`<sup>Required</sup> <a name="Uri" id="cdk-constructs.DockerImageName.property.uri"></a>

```go
func Uri() *string
```

- *Type:* *string

The uri of the docker image.

The uri spec follows https://github.com/containers/skopeo

---

##### `Creds`<sup>Optional</sup> <a name="Creds" id="cdk-constructs.DockerImageName.property.creds"></a>

```go
func Creds() *string
```

- *Type:* *string

The credentials of the docker image.

Format `user:password` or `AWS Secrets Manager secret arn` or `AWS Secrets Manager secret name`

---


### EndpointUtils <a name="EndpointUtils" id="cdk-constructs.EndpointUtils"></a>


#### Static Functions <a name="Static Functions" id="Static Functions"></a>

| **Name** | **Description** |
| --- | --- |
| <code><a href="#cdk-constructs.EndpointUtils.buildInternalServiceRecord">BuildInternalServiceRecord</a></code> | Builds the service DNS record from the service infos. |
| <code><a href="#cdk-constructs.EndpointUtils.buildInternalServiceRecordFirstPart">BuildInternalServiceRecordFirstPart</a></code> | Builds the service DNS record from the service infos. |
| <code><a href="#cdk-constructs.EndpointUtils.buildPrivateRoutingTokenPrefix">BuildPrivateRoutingTokenPrefix</a></code> | Build the routing token prefix for a private endpoint. |
| <code><a href="#cdk-constructs.EndpointUtils.buildPublicRoutingTokenPrefix">BuildPublicRoutingTokenPrefix</a></code> | Build the routing token prefix for a public endpoint. |
| <code><a href="#cdk-constructs.EndpointUtils.buildRoutingTokenPrefix">BuildRoutingTokenPrefix</a></code> | Build routing token prefix using Thron's conventions. |
| <code><a href="#cdk-constructs.EndpointUtils.buildServiceNameFromRoutingTokenPrefix">BuildServiceNameFromRoutingTokenPrefix</a></code> | Builds `serviceName` from routing token. |
| <code><a href="#cdk-constructs.EndpointUtils.isValidRoutingTokenPrefix">IsValidRoutingTokenPrefix</a></code> | Validates `routingTokenPrefix` against conventions. |
| <code><a href="#cdk-constructs.EndpointUtils.isValidThronServiceName">IsValidThronServiceName</a></code> | Check wether a service name validates against Thron conventions. |
| <code><a href="#cdk-constructs.EndpointUtils.isValidVersion">IsValidVersion</a></code> | Validates `version` against conventions. |

---

##### `BuildInternalServiceRecord` <a name="BuildInternalServiceRecord" id="cdk-constructs.EndpointUtils.buildInternalServiceRecord"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

cdkconstructs.EndpointUtils_BuildInternalServiceRecord(serviceName *string, internalDomain *string, sitename *string) *string
```

Builds the service DNS record from the service infos.

###### `serviceName`<sup>Required</sup> <a name="serviceName" id="cdk-constructs.EndpointUtils.buildInternalServiceRecord.parameter.serviceName"></a>

- *Type:* *string

the complete name of the service, i.e `awsd04-view-api-adxsso`.

---

###### `internalDomain`<sup>Required</sup> <a name="internalDomain" id="cdk-constructs.EndpointUtils.buildInternalServiceRecord.parameter.internalDomain"></a>

- *Type:* *string

the internal domain, i.e `cdndev.weebo.it`.

---

###### `sitename`<sup>Required</sup> <a name="sitename" id="cdk-constructs.EndpointUtils.buildInternalServiceRecord.parameter.sitename"></a>

- *Type:* *string

thron sitename, i.e. `awsd04`.

---

##### `BuildInternalServiceRecordFirstPart` <a name="BuildInternalServiceRecordFirstPart" id="cdk-constructs.EndpointUtils.buildInternalServiceRecordFirstPart"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

cdkconstructs.EndpointUtils_BuildInternalServiceRecordFirstPart(serviceName *string, internalDomain *string, sitename *string) *string
```

Builds the service DNS record from the service infos.

###### `serviceName`<sup>Required</sup> <a name="serviceName" id="cdk-constructs.EndpointUtils.buildInternalServiceRecordFirstPart.parameter.serviceName"></a>

- *Type:* *string

the complete name of the service, i.e `awsd04-view-api-adxsso`.

---

###### `internalDomain`<sup>Required</sup> <a name="internalDomain" id="cdk-constructs.EndpointUtils.buildInternalServiceRecordFirstPart.parameter.internalDomain"></a>

- *Type:* *string

the internal domain, i.e `cdndev.weebo.it`.

---

###### `sitename`<sup>Required</sup> <a name="sitename" id="cdk-constructs.EndpointUtils.buildInternalServiceRecordFirstPart.parameter.sitename"></a>

- *Type:* *string

thron sitename, i.e. `awsd04`.

---

##### `BuildPrivateRoutingTokenPrefix` <a name="BuildPrivateRoutingTokenPrefix" id="cdk-constructs.EndpointUtils.buildPrivateRoutingTokenPrefix"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

cdkconstructs.EndpointUtils_BuildPrivateRoutingTokenPrefix(serviceName *string, version *f64) *string
```

Build the routing token prefix for a private endpoint.

###### `serviceName`<sup>Required</sup> <a name="serviceName" id="cdk-constructs.EndpointUtils.buildPrivateRoutingTokenPrefix.parameter.serviceName"></a>

- *Type:* *string

---

###### `version`<sup>Required</sup> <a name="version" id="cdk-constructs.EndpointUtils.buildPrivateRoutingTokenPrefix.parameter.version"></a>

- *Type:* *f64

---

##### `BuildPublicRoutingTokenPrefix` <a name="BuildPublicRoutingTokenPrefix" id="cdk-constructs.EndpointUtils.buildPublicRoutingTokenPrefix"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

cdkconstructs.EndpointUtils_BuildPublicRoutingTokenPrefix(serviceName *string, version *f64) *string
```

Build the routing token prefix for a public endpoint.

###### `serviceName`<sup>Required</sup> <a name="serviceName" id="cdk-constructs.EndpointUtils.buildPublicRoutingTokenPrefix.parameter.serviceName"></a>

- *Type:* *string

---

###### `version`<sup>Required</sup> <a name="version" id="cdk-constructs.EndpointUtils.buildPublicRoutingTokenPrefix.parameter.version"></a>

- *Type:* *f64

---

##### `BuildRoutingTokenPrefix` <a name="BuildRoutingTokenPrefix" id="cdk-constructs.EndpointUtils.buildRoutingTokenPrefix"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

cdkconstructs.EndpointUtils_BuildRoutingTokenPrefix(serviceName *string, version *f64, visibility EndpointVisibility) *string
```

Build routing token prefix using Thron's conventions.

###### `serviceName`<sup>Required</sup> <a name="serviceName" id="cdk-constructs.EndpointUtils.buildRoutingTokenPrefix.parameter.serviceName"></a>

- *Type:* *string

---

###### `version`<sup>Required</sup> <a name="version" id="cdk-constructs.EndpointUtils.buildRoutingTokenPrefix.parameter.version"></a>

- *Type:* *f64

---

###### `visibility`<sup>Required</sup> <a name="visibility" id="cdk-constructs.EndpointUtils.buildRoutingTokenPrefix.parameter.visibility"></a>

- *Type:* <a href="#cdk-constructs.EndpointVisibility">EndpointVisibility</a>

---

##### `BuildServiceNameFromRoutingTokenPrefix` <a name="BuildServiceNameFromRoutingTokenPrefix" id="cdk-constructs.EndpointUtils.buildServiceNameFromRoutingTokenPrefix"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

cdkconstructs.EndpointUtils_BuildServiceNameFromRoutingTokenPrefix(routingTokenPrefix *string, serviceGroup ServiceGroup) *string
```

Builds `serviceName` from routing token.

###### `routingTokenPrefix`<sup>Required</sup> <a name="routingTokenPrefix" id="cdk-constructs.EndpointUtils.buildServiceNameFromRoutingTokenPrefix.parameter.routingTokenPrefix"></a>

- *Type:* *string

service routing token.

---

###### `serviceGroup`<sup>Required</sup> <a name="serviceGroup" id="cdk-constructs.EndpointUtils.buildServiceNameFromRoutingTokenPrefix.parameter.serviceGroup"></a>

- *Type:* <a href="#cdk-constructs.ServiceGroup">ServiceGroup</a>

service group.

---

##### `IsValidRoutingTokenPrefix` <a name="IsValidRoutingTokenPrefix" id="cdk-constructs.EndpointUtils.isValidRoutingTokenPrefix"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

cdkconstructs.EndpointUtils_IsValidRoutingTokenPrefix(routingTokenPrefix *string) *bool
```

Validates `routingTokenPrefix` against conventions.

###### `routingTokenPrefix`<sup>Required</sup> <a name="routingTokenPrefix" id="cdk-constructs.EndpointUtils.isValidRoutingTokenPrefix.parameter.routingTokenPrefix"></a>

- *Type:* *string

routing token prefix to validate.

---

##### `IsValidThronServiceName` <a name="IsValidThronServiceName" id="cdk-constructs.EndpointUtils.isValidThronServiceName"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

cdkconstructs.EndpointUtils_IsValidThronServiceName(serviceName *string) *bool
```

Check wether a service name validates against Thron conventions.

###### `serviceName`<sup>Required</sup> <a name="serviceName" id="cdk-constructs.EndpointUtils.isValidThronServiceName.parameter.serviceName"></a>

- *Type:* *string

---

##### `IsValidVersion` <a name="IsValidVersion" id="cdk-constructs.EndpointUtils.isValidVersion"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

cdkconstructs.EndpointUtils_IsValidVersion(version *f64) *bool
```

Validates `version` against conventions.

###### `version`<sup>Optional</sup> <a name="version" id="cdk-constructs.EndpointUtils.isValidVersion.parameter.version"></a>

- *Type:* *f64

---



### S3ArchiveName <a name="S3ArchiveName" id="cdk-constructs.S3ArchiveName"></a>

- *Implements:* <a href="#cdk-constructs.IImageName">IImageName</a>

#### Initializers <a name="Initializers" id="cdk-constructs.S3ArchiveName.Initializer"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

cdkconstructs.NewS3ArchiveName(p *string, ref *string, creds *string) S3ArchiveName
```

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.S3ArchiveName.Initializer.parameter.p">p</a></code> | <code>*string</code> | *No description.* |
| <code><a href="#cdk-constructs.S3ArchiveName.Initializer.parameter.ref">ref</a></code> | <code>*string</code> | *No description.* |
| <code><a href="#cdk-constructs.S3ArchiveName.Initializer.parameter.creds">creds</a></code> | <code>*string</code> | The credentials of the docker image. |

---

##### `p`<sup>Required</sup> <a name="p" id="cdk-constructs.S3ArchiveName.Initializer.parameter.p"></a>

- *Type:* *string

---

##### `ref`<sup>Optional</sup> <a name="ref" id="cdk-constructs.S3ArchiveName.Initializer.parameter.ref"></a>

- *Type:* *string

---

##### `creds`<sup>Optional</sup> <a name="creds" id="cdk-constructs.S3ArchiveName.Initializer.parameter.creds"></a>

- *Type:* *string

The credentials of the docker image.

Format `user:password` or `AWS Secrets Manager secret arn` or `AWS Secrets Manager secret name`

---



#### Properties <a name="Properties" id="Properties"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.S3ArchiveName.property.uri">Uri</a></code> | <code>*string</code> | The uri of the docker image. |
| <code><a href="#cdk-constructs.S3ArchiveName.property.creds">Creds</a></code> | <code>*string</code> | The credentials of the docker image. |

---

##### `Uri`<sup>Required</sup> <a name="Uri" id="cdk-constructs.S3ArchiveName.property.uri"></a>

```go
func Uri() *string
```

- *Type:* *string

The uri of the docker image.

The uri spec follows https://github.com/containers/skopeo

---

##### `Creds`<sup>Optional</sup> <a name="Creds" id="cdk-constructs.S3ArchiveName.property.creds"></a>

```go
func Creds() *string
```

- *Type:* *string

The credentials of the docker image.

Format `user:password` or `AWS Secrets Manager secret arn` or `AWS Secrets Manager secret name`

---


### ThronApiGatewayUtils <a name="ThronApiGatewayUtils" id="cdk-constructs.ThronApiGatewayUtils"></a>


#### Static Functions <a name="Static Functions" id="Static Functions"></a>

| **Name** | **Description** |
| --- | --- |
| <code><a href="#cdk-constructs.ThronApiGatewayUtils.apigwMainIdSsmParam">ApigwMainIdSsmParam</a></code> | *No description.* |
| <code><a href="#cdk-constructs.ThronApiGatewayUtils.apigwVpceDnsSsmParam">ApigwVpceDnsSsmParam</a></code> | *No description.* |
| <code><a href="#cdk-constructs.ThronApiGatewayUtils.apigwVpceIdSsmParam">ApigwVpceIdSsmParam</a></code> | *No description.* |
| <code><a href="#cdk-constructs.ThronApiGatewayUtils.certificateIdArnSsmParam">CertificateIdArnSsmParam</a></code> | *No description.* |
| <code><a href="#cdk-constructs.ThronApiGatewayUtils.sanitizeId">SanitizeId</a></code> | *No description.* |

---

##### `ApigwMainIdSsmParam` <a name="ApigwMainIdSsmParam" id="cdk-constructs.ThronApiGatewayUtils.apigwMainIdSsmParam"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

cdkconstructs.ThronApiGatewayUtils_ApigwMainIdSsmParam(thronSitename *string) *string
```

###### `thronSitename`<sup>Required</sup> <a name="thronSitename" id="cdk-constructs.ThronApiGatewayUtils.apigwMainIdSsmParam.parameter.thronSitename"></a>

- *Type:* *string

---

##### `ApigwVpceDnsSsmParam` <a name="ApigwVpceDnsSsmParam" id="cdk-constructs.ThronApiGatewayUtils.apigwVpceDnsSsmParam"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

cdkconstructs.ThronApiGatewayUtils_ApigwVpceDnsSsmParam(thronSitename *string) *string
```

###### `thronSitename`<sup>Required</sup> <a name="thronSitename" id="cdk-constructs.ThronApiGatewayUtils.apigwVpceDnsSsmParam.parameter.thronSitename"></a>

- *Type:* *string

---

##### `ApigwVpceIdSsmParam` <a name="ApigwVpceIdSsmParam" id="cdk-constructs.ThronApiGatewayUtils.apigwVpceIdSsmParam"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

cdkconstructs.ThronApiGatewayUtils_ApigwVpceIdSsmParam(thronSitename *string) *string
```

###### `thronSitename`<sup>Required</sup> <a name="thronSitename" id="cdk-constructs.ThronApiGatewayUtils.apigwVpceIdSsmParam.parameter.thronSitename"></a>

- *Type:* *string

---

##### `CertificateIdArnSsmParam` <a name="CertificateIdArnSsmParam" id="cdk-constructs.ThronApiGatewayUtils.certificateIdArnSsmParam"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

cdkconstructs.ThronApiGatewayUtils_CertificateIdArnSsmParam(thronSitename *string) *string
```

###### `thronSitename`<sup>Required</sup> <a name="thronSitename" id="cdk-constructs.ThronApiGatewayUtils.certificateIdArnSsmParam.parameter.thronSitename"></a>

- *Type:* *string

---

##### `SanitizeId` <a name="SanitizeId" id="cdk-constructs.ThronApiGatewayUtils.sanitizeId"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

cdkconstructs.ThronApiGatewayUtils_SanitizeId(id *string) *string
```

###### `id`<sup>Required</sup> <a name="id" id="cdk-constructs.ThronApiGatewayUtils.sanitizeId.parameter.id"></a>

- *Type:* *string

---



### ThronEnvironment <a name="ThronEnvironment" id="cdk-constructs.ThronEnvironment"></a>

#### Initializers <a name="Initializers" id="cdk-constructs.ThronEnvironment.Initializer"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

cdkconstructs.NewThronEnvironment() ThronEnvironment
```

| **Name** | **Type** | **Description** |
| --- | --- | --- |

---




#### Constants <a name="Constants" id="Constants"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.ThronEnvironment.property.BETA">Beta</a></code> | <code>*string</code> | *No description.* |
| <code><a href="#cdk-constructs.ThronEnvironment.property.DEVELOPMENT">Development</a></code> | <code>*string</code> | *No description.* |
| <code><a href="#cdk-constructs.ThronEnvironment.property.PRODUCTION">Production</a></code> | <code>*string</code> | *No description.* |
| <code><a href="#cdk-constructs.ThronEnvironment.property.QUALITY">Quality</a></code> | <code>*string</code> | *No description.* |

---

##### `Beta`<sup>Required</sup> <a name="Beta" id="cdk-constructs.ThronEnvironment.property.BETA"></a>

```go
func Beta() *string
```

- *Type:* *string

---

##### `Development`<sup>Required</sup> <a name="Development" id="cdk-constructs.ThronEnvironment.property.DEVELOPMENT"></a>

```go
func Development() *string
```

- *Type:* *string

---

##### `Production`<sup>Required</sup> <a name="Production" id="cdk-constructs.ThronEnvironment.property.PRODUCTION"></a>

```go
func Production() *string
```

- *Type:* *string

---

##### `Quality`<sup>Required</sup> <a name="Quality" id="cdk-constructs.ThronEnvironment.property.QUALITY"></a>

```go
func Quality() *string
```

- *Type:* *string

---

### ThronHealthCheck <a name="ThronHealthCheck" id="cdk-constructs.ThronHealthCheck"></a>

#### Initializers <a name="Initializers" id="cdk-constructs.ThronHealthCheck.Initializer"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

cdkconstructs.NewThronHealthCheck() ThronHealthCheck
```

| **Name** | **Type** | **Description** |
| --- | --- | --- |

---


#### Static Functions <a name="Static Functions" id="Static Functions"></a>

| **Name** | **Description** |
| --- | --- |
| <code><a href="#cdk-constructs.ThronHealthCheck.default">Default</a></code> | *No description.* |
| <code><a href="#cdk-constructs.ThronHealthCheck.defaultWithOverrides">DefaultWithOverrides</a></code> | *No description.* |

---

##### `Default` <a name="Default" id="cdk-constructs.ThronHealthCheck.default"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

cdkconstructs.ThronHealthCheck_Default() HealthCheck
```

##### `DefaultWithOverrides` <a name="DefaultWithOverrides" id="cdk-constructs.ThronHealthCheck.defaultWithOverrides"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

cdkconstructs.ThronHealthCheck_DefaultWithOverrides(props ThronHealthCheckOverride) HealthCheck
```

###### `props`<sup>Required</sup> <a name="props" id="cdk-constructs.ThronHealthCheck.defaultWithOverrides.parameter.props"></a>

- *Type:* <a href="#cdk-constructs.ThronHealthCheckOverride">ThronHealthCheckOverride</a>

---



### ThronLambdaSingleEnvPipelineBuilder <a name="ThronLambdaSingleEnvPipelineBuilder" id="cdk-constructs.ThronLambdaSingleEnvPipelineBuilder"></a>

Builder Class for {@link ThronLambdaSingleEnvPipeline}.

#### Initializers <a name="Initializers" id="cdk-constructs.ThronLambdaSingleEnvPipelineBuilder.Initializer"></a>

```go
import "git-codecommit.eu-west-1.amazonaws.com/v1/repos/cdk-constructs-go.git/cdkconstructs"

cdkconstructs.NewThronLambdaSingleEnvPipelineBuilder() ThronLambdaSingleEnvPipelineBuilder
```

| **Name** | **Type** | **Description** |
| --- | --- | --- |

---

#### Methods <a name="Methods" id="Methods"></a>

| **Name** | **Description** |
| --- | --- |
| <code><a href="#cdk-constructs.ThronLambdaSingleEnvPipelineBuilder.buildPipeline">BuildPipeline</a></code> | *No description.* |
| <code><a href="#cdk-constructs.ThronLambdaSingleEnvPipelineBuilder.withArtifactBucket">WithArtifactBucket</a></code> | *No description.* |
| <code><a href="#cdk-constructs.ThronLambdaSingleEnvPipelineBuilder.withBuildDisabled">WithBuildDisabled</a></code> | *No description.* |
| <code><a href="#cdk-constructs.ThronLambdaSingleEnvPipelineBuilder.withDefaultBuildStepConfig">WithDefaultBuildStepConfig</a></code> | *No description.* |
| <code><a href="#cdk-constructs.ThronLambdaSingleEnvPipelineBuilder.withDefaultDeployStepConfig">WithDefaultDeployStepConfig</a></code> | *No description.* |
| <code><a href="#cdk-constructs.ThronLambdaSingleEnvPipelineBuilder.withDefaultStepConfig">WithDefaultStepConfig</a></code> | *No description.* |
| <code><a href="#cdk-constructs.ThronLambdaSingleEnvPipelineBuilder.withDefaultTestStepConfig">WithDefaultTestStepConfig</a></code> | *No description.* |
| <code><a href="#cdk-constructs.ThronLambdaSingleEnvPipelineBuilder.withDeployEnvironment">WithDeployEnvironment</a></code> | *No description.* |
| <code><a href="#cdk-constructs.ThronLambdaSingleEnvPipelineBuilder.withLambda">WithLambda</a></code> | *No description.* |
| <code><a href="#cdk-constructs.ThronLambdaSingleEnvPipelineBuilder.withNotifyConfig">WithNotifyConfig</a></code> | *No description.* |
| <code><a href="#cdk-constructs.ThronLambdaSingleEnvPipelineBuilder.withSourceConfiguration">WithSourceConfiguration</a></code> | *No description.* |
| <code><a href="#cdk-constructs.ThronLambdaSingleEnvPipelineBuilder.withTestStep">WithTestStep</a></code> | *No description.* |

---

##### `BuildPipeline` <a name="BuildPipeline" id="cdk-constructs.ThronLambdaSingleEnvPipelineBuilder.buildPipeline"></a>

```go
func BuildPipeline(scope Construct, id *string, prefix *string) ThronLambdaSingleEnvPipeline
```

###### `scope`<sup>Required</sup> <a name="scope" id="cdk-constructs.ThronLambdaSingleEnvPipelineBuilder.buildPipeline.parameter.scope"></a>

- *Type:* github.com/aws/constructs-go/constructs/v10.Construct

---

###### `id`<sup>Required</sup> <a name="id" id="cdk-constructs.ThronLambdaSingleEnvPipelineBuilder.buildPipeline.parameter.id"></a>

- *Type:* *string

---

###### `prefix`<sup>Required</sup> <a name="prefix" id="cdk-constructs.ThronLambdaSingleEnvPipelineBuilder.buildPipeline.parameter.prefix"></a>

- *Type:* *string

---

##### `WithArtifactBucket` <a name="WithArtifactBucket" id="cdk-constructs.ThronLambdaSingleEnvPipelineBuilder.withArtifactBucket"></a>

```go
func WithArtifactBucket(artifactBucket IBucket) ThronLambdaSingleEnvPipelineBuilder
```

###### `artifactBucket`<sup>Required</sup> <a name="artifactBucket" id="cdk-constructs.ThronLambdaSingleEnvPipelineBuilder.withArtifactBucket.parameter.artifactBucket"></a>

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_s3.IBucket

---

##### `WithBuildDisabled` <a name="WithBuildDisabled" id="cdk-constructs.ThronLambdaSingleEnvPipelineBuilder.withBuildDisabled"></a>

```go
func WithBuildDisabled() ThronLambdaSingleEnvPipelineBuilder
```

##### `WithDefaultBuildStepConfig` <a name="WithDefaultBuildStepConfig" id="cdk-constructs.ThronLambdaSingleEnvPipelineBuilder.withDefaultBuildStepConfig"></a>

```go
func WithDefaultBuildStepConfig(stepConfig StepConfig) ThronLambdaSingleEnvPipelineBuilder
```

###### `stepConfig`<sup>Required</sup> <a name="stepConfig" id="cdk-constructs.ThronLambdaSingleEnvPipelineBuilder.withDefaultBuildStepConfig.parameter.stepConfig"></a>

- *Type:* <a href="#cdk-constructs.StepConfig">StepConfig</a>

---

##### `WithDefaultDeployStepConfig` <a name="WithDefaultDeployStepConfig" id="cdk-constructs.ThronLambdaSingleEnvPipelineBuilder.withDefaultDeployStepConfig"></a>

```go
func WithDefaultDeployStepConfig(stepConfig StepConfig) ThronLambdaSingleEnvPipelineBuilder
```

###### `stepConfig`<sup>Required</sup> <a name="stepConfig" id="cdk-constructs.ThronLambdaSingleEnvPipelineBuilder.withDefaultDeployStepConfig.parameter.stepConfig"></a>

- *Type:* <a href="#cdk-constructs.StepConfig">StepConfig</a>

---

##### `WithDefaultStepConfig` <a name="WithDefaultStepConfig" id="cdk-constructs.ThronLambdaSingleEnvPipelineBuilder.withDefaultStepConfig"></a>

```go
func WithDefaultStepConfig(stepConfig StepConfig) ThronLambdaSingleEnvPipelineBuilder
```

###### `stepConfig`<sup>Required</sup> <a name="stepConfig" id="cdk-constructs.ThronLambdaSingleEnvPipelineBuilder.withDefaultStepConfig.parameter.stepConfig"></a>

- *Type:* <a href="#cdk-constructs.StepConfig">StepConfig</a>

---

##### `WithDefaultTestStepConfig` <a name="WithDefaultTestStepConfig" id="cdk-constructs.ThronLambdaSingleEnvPipelineBuilder.withDefaultTestStepConfig"></a>

```go
func WithDefaultTestStepConfig(stepConfig StepConfig) ThronLambdaSingleEnvPipelineBuilder
```

###### `stepConfig`<sup>Required</sup> <a name="stepConfig" id="cdk-constructs.ThronLambdaSingleEnvPipelineBuilder.withDefaultTestStepConfig.parameter.stepConfig"></a>

- *Type:* <a href="#cdk-constructs.StepConfig">StepConfig</a>

---

##### `WithDeployEnvironment` <a name="WithDeployEnvironment" id="cdk-constructs.ThronLambdaSingleEnvPipelineBuilder.withDeployEnvironment"></a>

```go
func WithDeployEnvironment(deployConfig DeployConfig) ThronLambdaSingleEnvPipelineBuilder
```

###### `deployConfig`<sup>Required</sup> <a name="deployConfig" id="cdk-constructs.ThronLambdaSingleEnvPipelineBuilder.withDeployEnvironment.parameter.deployConfig"></a>

- *Type:* <a href="#cdk-constructs.DeployConfig">DeployConfig</a>

---

##### `WithLambda` <a name="WithLambda" id="cdk-constructs.ThronLambdaSingleEnvPipelineBuilder.withLambda"></a>

```go
func WithLambda(lambdaId *string, destinationEcrRepository Repository, stepConfOverrides StepConfig) ThronLambdaSingleEnvPipelineBuilder
```

###### `lambdaId`<sup>Required</sup> <a name="lambdaId" id="cdk-constructs.ThronLambdaSingleEnvPipelineBuilder.withLambda.parameter.lambdaId"></a>

- *Type:* *string

---

###### `destinationEcrRepository`<sup>Required</sup> <a name="destinationEcrRepository" id="cdk-constructs.ThronLambdaSingleEnvPipelineBuilder.withLambda.parameter.destinationEcrRepository"></a>

- *Type:* github.com/aws/aws-cdk-go/awscdk/v2.aws_ecr.Repository

---

###### `stepConfOverrides`<sup>Optional</sup> <a name="stepConfOverrides" id="cdk-constructs.ThronLambdaSingleEnvPipelineBuilder.withLambda.parameter.stepConfOverrides"></a>

- *Type:* <a href="#cdk-constructs.StepConfig">StepConfig</a>

---

##### `WithNotifyConfig` <a name="WithNotifyConfig" id="cdk-constructs.ThronLambdaSingleEnvPipelineBuilder.withNotifyConfig"></a>

```go
func WithNotifyConfig(notifyConf NotifyConf) ThronLambdaSingleEnvPipelineBuilder
```

###### `notifyConf`<sup>Required</sup> <a name="notifyConf" id="cdk-constructs.ThronLambdaSingleEnvPipelineBuilder.withNotifyConfig.parameter.notifyConf"></a>

- *Type:* <a href="#cdk-constructs.NotifyConf">NotifyConf</a>

---

##### `WithSourceConfiguration` <a name="WithSourceConfiguration" id="cdk-constructs.ThronLambdaSingleEnvPipelineBuilder.withSourceConfiguration"></a>

```go
func WithSourceConfiguration(sourceConfig ThronLambdaSingleEnvPipelineCodeCommitProps) ThronLambdaSingleEnvPipelineBuilder
```

###### `sourceConfig`<sup>Required</sup> <a name="sourceConfig" id="cdk-constructs.ThronLambdaSingleEnvPipelineBuilder.withSourceConfiguration.parameter.sourceConfig"></a>

- *Type:* <a href="#cdk-constructs.ThronLambdaSingleEnvPipelineCodeCommitProps">ThronLambdaSingleEnvPipelineCodeCommitProps</a>

---

##### `WithTestStep` <a name="WithTestStep" id="cdk-constructs.ThronLambdaSingleEnvPipelineBuilder.withTestStep"></a>

```go
func WithTestStep(testId *string, stepConfOverrides StepConfig) ThronLambdaSingleEnvPipelineBuilder
```

###### `testId`<sup>Required</sup> <a name="testId" id="cdk-constructs.ThronLambdaSingleEnvPipelineBuilder.withTestStep.parameter.testId"></a>

- *Type:* *string

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

```go
func DefaultStepConfig() StepConfig
```

- *Type:* <a href="#cdk-constructs.StepConfig">StepConfig</a>

---

## Protocols <a name="Protocols" id="Protocols"></a>

### IImageName <a name="IImageName" id="cdk-constructs.IImageName"></a>

- *Implemented By:* <a href="#cdk-constructs.DockerImageName">DockerImageName</a>, <a href="#cdk-constructs.S3ArchiveName">S3ArchiveName</a>, <a href="#cdk-constructs.IImageName">IImageName</a>


#### Properties <a name="Properties" id="Properties"></a>

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| <code><a href="#cdk-constructs.IImageName.property.uri">Uri</a></code> | <code>*string</code> | The uri of the docker image. |
| <code><a href="#cdk-constructs.IImageName.property.creds">Creds</a></code> | <code>*string</code> | The credentials of the docker image. |

---

##### `Uri`<sup>Required</sup> <a name="Uri" id="cdk-constructs.IImageName.property.uri"></a>

```go
func Uri() *string
```

- *Type:* *string

The uri of the docker image.

The uri spec follows https://github.com/containers/skopeo

---

##### `Creds`<sup>Optional</sup> <a name="Creds" id="cdk-constructs.IImageName.property.creds"></a>

```go
func Creds() *string
```

- *Type:* *string

The credentials of the docker image.

Format `user:password` or `AWS Secrets Manager secret arn` or `AWS Secrets Manager secret name`

---

## Enums <a name="Enums" id="Enums"></a>

### AvailabilityZone <a name="AvailabilityZone" id="cdk-constructs.AvailabilityZone"></a>

Enum with all the AZ you may use in a region.

#### Members <a name="Members" id="Members"></a>

| **Name** | **Description** |
| --- | --- |
| <code><a href="#cdk-constructs.AvailabilityZone.A">AvailabilityZone_A</a></code> | *No description.* |
| <code><a href="#cdk-constructs.AvailabilityZone.B">AvailabilityZone_B</a></code> | *No description.* |
| <code><a href="#cdk-constructs.AvailabilityZone.C">AvailabilityZone_C</a></code> | *No description.* |
| <code><a href="#cdk-constructs.AvailabilityZone.D">AvailabilityZone_D</a></code> | *No description.* |

---

##### `AvailabilityZone_A` <a name="AvailabilityZone_A" id="cdk-constructs.AvailabilityZone.A"></a>

---


##### `AvailabilityZone_B` <a name="AvailabilityZone_B" id="cdk-constructs.AvailabilityZone.B"></a>

---


##### `AvailabilityZone_C` <a name="AvailabilityZone_C" id="cdk-constructs.AvailabilityZone.C"></a>

---


##### `AvailabilityZone_D` <a name="AvailabilityZone_D" id="cdk-constructs.AvailabilityZone.D"></a>

---


### ClusterOption <a name="ClusterOption" id="cdk-constructs.ClusterOption"></a>

#### Members <a name="Members" id="Members"></a>

| **Name** | **Description** |
| --- | --- |
| <code><a href="#cdk-constructs.ClusterOption.CORE_MAIN">ClusterOption_CORE_MAIN</a></code> | *No description.* |
| <code><a href="#cdk-constructs.ClusterOption.ECS_MANAGEMENT">ClusterOption_ECS_MANAGEMENT</a></code> | *No description.* |
| <code><a href="#cdk-constructs.ClusterOption.THE_SHIRE">ClusterOption_THE_SHIRE</a></code> | *No description.* |
| <code><a href="#cdk-constructs.ClusterOption.VALINOR">ClusterOption_VALINOR</a></code> | *No description.* |

---

##### `ClusterOption_CORE_MAIN` <a name="ClusterOption_CORE_MAIN" id="cdk-constructs.ClusterOption.CORE_MAIN"></a>

---


##### `ClusterOption_ECS_MANAGEMENT` <a name="ClusterOption_ECS_MANAGEMENT" id="cdk-constructs.ClusterOption.ECS_MANAGEMENT"></a>

---


##### `ClusterOption_THE_SHIRE` <a name="ClusterOption_THE_SHIRE" id="cdk-constructs.ClusterOption.THE_SHIRE"></a>

---


##### `ClusterOption_VALINOR` <a name="ClusterOption_VALINOR" id="cdk-constructs.ClusterOption.VALINOR"></a>

---


### EndpointVisibility <a name="EndpointVisibility" id="cdk-constructs.EndpointVisibility"></a>

#### Members <a name="Members" id="Members"></a>

| **Name** | **Description** |
| --- | --- |
| <code><a href="#cdk-constructs.EndpointVisibility.PUBLIC">EndpointVisibility_PUBLIC</a></code> | *No description.* |
| <code><a href="#cdk-constructs.EndpointVisibility.PRIVATE">EndpointVisibility_PRIVATE</a></code> | *No description.* |

---

##### `EndpointVisibility_PUBLIC` <a name="EndpointVisibility_PUBLIC" id="cdk-constructs.EndpointVisibility.PUBLIC"></a>

---


##### `EndpointVisibility_PRIVATE` <a name="EndpointVisibility_PRIVATE" id="cdk-constructs.EndpointVisibility.PRIVATE"></a>

---


### NewRelicIgnoreExtensionChecksOption <a name="NewRelicIgnoreExtensionChecksOption" id="cdk-constructs.NewRelicIgnoreExtensionChecksOption"></a>

#### Members <a name="Members" id="Members"></a>

| **Name** | **Description** |
| --- | --- |
| <code><a href="#cdk-constructs.NewRelicIgnoreExtensionChecksOption.ALL">NewRelicIgnoreExtensionChecksOption_ALL</a></code> | *No description.* |
| <code><a href="#cdk-constructs.NewRelicIgnoreExtensionChecksOption.AGENT">NewRelicIgnoreExtensionChecksOption_AGENT</a></code> | *No description.* |
| <code><a href="#cdk-constructs.NewRelicIgnoreExtensionChecksOption.HANDLER">NewRelicIgnoreExtensionChecksOption_HANDLER</a></code> | *No description.* |
| <code><a href="#cdk-constructs.NewRelicIgnoreExtensionChecksOption.SANITY">NewRelicIgnoreExtensionChecksOption_SANITY</a></code> | *No description.* |
| <code><a href="#cdk-constructs.NewRelicIgnoreExtensionChecksOption.VENDOR">NewRelicIgnoreExtensionChecksOption_VENDOR</a></code> | *No description.* |
| <code><a href="#cdk-constructs.NewRelicIgnoreExtensionChecksOption.FALSE">NewRelicIgnoreExtensionChecksOption_FALSE</a></code> | *No description.* |

---

##### `NewRelicIgnoreExtensionChecksOption_ALL` <a name="NewRelicIgnoreExtensionChecksOption_ALL" id="cdk-constructs.NewRelicIgnoreExtensionChecksOption.ALL"></a>

---


##### `NewRelicIgnoreExtensionChecksOption_AGENT` <a name="NewRelicIgnoreExtensionChecksOption_AGENT" id="cdk-constructs.NewRelicIgnoreExtensionChecksOption.AGENT"></a>

---


##### `NewRelicIgnoreExtensionChecksOption_HANDLER` <a name="NewRelicIgnoreExtensionChecksOption_HANDLER" id="cdk-constructs.NewRelicIgnoreExtensionChecksOption.HANDLER"></a>

---


##### `NewRelicIgnoreExtensionChecksOption_SANITY` <a name="NewRelicIgnoreExtensionChecksOption_SANITY" id="cdk-constructs.NewRelicIgnoreExtensionChecksOption.SANITY"></a>

---


##### `NewRelicIgnoreExtensionChecksOption_VENDOR` <a name="NewRelicIgnoreExtensionChecksOption_VENDOR" id="cdk-constructs.NewRelicIgnoreExtensionChecksOption.VENDOR"></a>

---


##### `NewRelicIgnoreExtensionChecksOption_FALSE` <a name="NewRelicIgnoreExtensionChecksOption_FALSE" id="cdk-constructs.NewRelicIgnoreExtensionChecksOption.FALSE"></a>

---


### PipelineCapability <a name="PipelineCapability" id="cdk-constructs.PipelineCapability"></a>

#### Members <a name="Members" id="Members"></a>

| **Name** | **Description** |
| --- | --- |
| <code><a href="#cdk-constructs.PipelineCapability.BUILD">PipelineCapability_BUILD</a></code> | Enable BUILD stage in the pipeline. |
| <code><a href="#cdk-constructs.PipelineCapability.TEST">PipelineCapability_TEST</a></code> | Enable TEST stage in the pipeline. |
| <code><a href="#cdk-constructs.PipelineCapability.NOTIFY_ON_START">PipelineCapability_NOTIFY_ON_START</a></code> | Enable pipeline notification when the pipeline starts, both manually or via a new commit. |
| <code><a href="#cdk-constructs.PipelineCapability.NOTIFY_ON_FAIL">PipelineCapability_NOTIFY_ON_FAIL</a></code> | Enable pipeline notification when the pipeline fails. |
| <code><a href="#cdk-constructs.PipelineCapability.NOTIFY_ON_SUCCESS">PipelineCapability_NOTIFY_ON_SUCCESS</a></code> | Enable pipeline notification when the pipeline succeeds. |

---

##### `PipelineCapability_BUILD` <a name="PipelineCapability_BUILD" id="cdk-constructs.PipelineCapability.BUILD"></a>

Enable BUILD stage in the pipeline.

---


##### `PipelineCapability_TEST` <a name="PipelineCapability_TEST" id="cdk-constructs.PipelineCapability.TEST"></a>

Enable TEST stage in the pipeline.

---


##### `PipelineCapability_NOTIFY_ON_START` <a name="PipelineCapability_NOTIFY_ON_START" id="cdk-constructs.PipelineCapability.NOTIFY_ON_START"></a>

Enable pipeline notification when the pipeline starts, both manually or via a new commit.

---


##### `PipelineCapability_NOTIFY_ON_FAIL` <a name="PipelineCapability_NOTIFY_ON_FAIL" id="cdk-constructs.PipelineCapability.NOTIFY_ON_FAIL"></a>

Enable pipeline notification when the pipeline fails.

---


##### `PipelineCapability_NOTIFY_ON_SUCCESS` <a name="PipelineCapability_NOTIFY_ON_SUCCESS" id="cdk-constructs.PipelineCapability.NOTIFY_ON_SUCCESS"></a>

Enable pipeline notification when the pipeline succeeds.

---


### ServiceGroup <a name="ServiceGroup" id="cdk-constructs.ServiceGroup"></a>

#### Members <a name="Members" id="Members"></a>

| **Name** | **Description** |
| --- | --- |
| <code><a href="#cdk-constructs.ServiceGroup.PRODUCT">ServiceGroup_PRODUCT</a></code> | *No description.* |
| <code><a href="#cdk-constructs.ServiceGroup.VIEW">ServiceGroup_VIEW</a></code> | *No description.* |

---

##### `ServiceGroup_PRODUCT` <a name="ServiceGroup_PRODUCT" id="cdk-constructs.ServiceGroup.PRODUCT"></a>

---


##### `ServiceGroup_VIEW` <a name="ServiceGroup_VIEW" id="cdk-constructs.ServiceGroup.VIEW"></a>

---


### SubnetType <a name="SubnetType" id="cdk-constructs.SubnetType"></a>

Attribute indicating whether a Subnet is public or private.

#### Members <a name="Members" id="Members"></a>

| **Name** | **Description** |
| --- | --- |
| <code><a href="#cdk-constructs.SubnetType.PUBLIC">SubnetType_PUBLIC</a></code> | *No description.* |
| <code><a href="#cdk-constructs.SubnetType.PRIVATE">SubnetType_PRIVATE</a></code> | *No description.* |

---

##### `SubnetType_PUBLIC` <a name="SubnetType_PUBLIC" id="cdk-constructs.SubnetType.PUBLIC"></a>

---


##### `SubnetType_PRIVATE` <a name="SubnetType_PRIVATE" id="cdk-constructs.SubnetType.PRIVATE"></a>

---

