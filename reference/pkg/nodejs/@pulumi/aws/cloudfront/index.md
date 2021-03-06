---
title: Module cloudfront
---

<a href="../index.html">@pulumi/aws</a> &gt; cloudfront

<h2 class="pdoc-module-header">Index</h2>

* <a href="#Distribution">class Distribution</a>
* <a href="#OriginAccessIdentity">class OriginAccessIdentity</a>
* <a href="#DistributionArgs">interface DistributionArgs</a>
* <a href="#DistributionState">interface DistributionState</a>
* <a href="#OriginAccessIdentityArgs">interface OriginAccessIdentityArgs</a>
* <a href="#OriginAccessIdentityState">interface OriginAccessIdentityState</a>

<a href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/cloudfront/distribution.ts">cloudfront/distribution.ts</a> <a href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/cloudfront/originAccessIdentity.ts">cloudfront/originAccessIdentity.ts</a> 


<h2 class="pdoc-module-header" id="Distribution">
<a class="pdoc-member-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/cloudfront/distribution.ts#L21">class Distribution</a>
</h2>

Creates an Amazon CloudFront web distribution.

For information about CloudFront distributions, see the
[Amazon CloudFront Developer Guide][1]. For specific information about creating
CloudFront web distributions, see the [POST Distribution][2] page in the Amazon
CloudFront API Reference.

~> **NOTE:** CloudFront distributions take about 15 minutes to a deployed state
after creation or modification. During this time, deletes to resources will be
blocked. If you need to delete a distribution that is enabled and you do not
want to wait, you need to use the `retain_on_delete` flag.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/cloudfront/distribution.ts#L171">constructor</a>
</h3>

```typescript
new Distribution(name: string, args: DistributionArgs, opts?: pulumi.CustomResourceOptions)
```


Create a Distribution resource with the given unique name, arguments, and options.

* `name` The _unique_ name of the resource.
* `args` The arguments to use to populate this resource&#39;s properties.
* `opts` A bag of options that control this resource&#39;s behavior.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/cloudfront/distribution.ts#L30">method get</a>
</h3>

```typescript
public static get(name: string, id: pulumi.Input<pulumi.ID>, state?: DistributionState): Distribution
```


Get an existing Distribution resource's state with the given name, ID, and optional extra
properties used to qualify the lookup.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/node_modules/@pulumi/pulumi/resource.d.ts#L13">method getProvider</a>
</h3>

```typescript
getProvider(moduleMember: string): ProviderResource | undefined
```

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/node_modules/@pulumi/pulumi/resource.d.ts#L85">method isInstance</a>
</h3>

```typescript
static isInstance(obj: any): boolean
```


Returns true if the given object is an instance of CustomResource.  This is designed to work even when
multiple copies of the Pulumi SDK have been loaded into the same process.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/cloudfront/distribution.ts#L39">property activeTrustedSigners</a>
</h3>

```typescript
public activeTrustedSigners: pulumi.Output<{ ... }>;
```


The key pair IDs that CloudFront is aware of for
each trusted signer, if the distribution is set up to serve private content
with signed URLs.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/cloudfront/distribution.ts#L44">property aliases</a>
</h3>

```typescript
public aliases: pulumi.Output<string[] | undefined>;
```


Extra CNAMEs (alternate domain names), if any, for
this distribution.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/cloudfront/distribution.ts#L48">property arn</a>
</h3>

```typescript
public arn: pulumi.Output<string>;
```


The ARN (Amazon Resource Name) for the distribution. For example: arn:aws:cloudfront::123456789012:distribution/EDFDVBD632BHDS5, where 123456789012 is your AWS account ID.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/cloudfront/distribution.ts#L52">property cacheBehaviors</a>
</h3>

```typescript
public cacheBehaviors: pulumi.Output<{ ... }[] | undefined>;
```


**Deprecated**, use `ordered_cache_behavior` instead.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/cloudfront/distribution.ts#L57">property callerReference</a>
</h3>

```typescript
public callerReference: pulumi.Output<string>;
```


Internal value used by CloudFront to allow future
updates to the distribution configuration.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/cloudfront/distribution.ts#L62">property comment</a>
</h3>

```typescript
public comment: pulumi.Output<string | undefined>;
```


Any comments you want to include about the
distribution.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/cloudfront/distribution.ts#L66">property customErrorResponses</a>
</h3>

```typescript
public customErrorResponses: pulumi.Output<{ ... }[] | undefined>;
```


One or more [custom error response](#custom-error-response-arguments) elements (multiples allowed).

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/cloudfront/distribution.ts#L71">property defaultCacheBehavior</a>
</h3>

```typescript
public defaultCacheBehavior: pulumi.Output<{ ... }>;
```


The [default cache behavior](#default-cache-behavior-arguments) for this distribution (maximum
one).

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/cloudfront/distribution.ts#L76">property defaultRootObject</a>
</h3>

```typescript
public defaultRootObject: pulumi.Output<string | undefined>;
```


The object that you want CloudFront to
return (for example, index.html) when an end user requests the root URL.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/cloudfront/distribution.ts#L81">property domainName</a>
</h3>

```typescript
public domainName: pulumi.Output<string>;
```


The DNS domain name of either the S3 bucket, or
web site of your custom origin.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/cloudfront/distribution.ts#L86">property enabled</a>
</h3>

```typescript
public enabled: pulumi.Output<boolean>;
```


Whether the distribution is enabled to accept end
user requests for content.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/cloudfront/distribution.ts#L91">property etag</a>
</h3>

```typescript
public etag: pulumi.Output<string>;
```


The current version of the distribution's information. For example:
`E2QWRUHAPOMQZL`.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/cloudfront/distribution.ts#L97">property hostedZoneId</a>
</h3>

```typescript
public hostedZoneId: pulumi.Output<string>;
```


The CloudFront Route 53 zone ID that can be used to
route an [Alias Resource Record Set][7] to. This attribute is simply an
alias for the zone ID `Z2FDTNDATAQYW2`.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/cloudfront/distribution.ts#L103">property httpVersion</a>
</h3>

```typescript
public httpVersion: pulumi.Output<string | undefined>;
```


The maximum HTTP version to support on the
distribution. Allowed values are `http1.1` and `http2`. The default is
`http2`.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/node_modules/@pulumi/pulumi/resource.d.ts#L80">property id</a>
</h3>

```typescript
id: Output<ID>;
```


id is the provider-assigned unique ID for this managed resource.  It is set during
deployments and may be missing (undefined) during planning phases.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/cloudfront/distribution.ts#L108">property inProgressValidationBatches</a>
</h3>

```typescript
public inProgressValidationBatches: pulumi.Output<number>;
```


The number of invalidation batches
currently in progress.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/cloudfront/distribution.ts#L112">property isIpv6Enabled</a>
</h3>

```typescript
public isIpv6Enabled: pulumi.Output<boolean | undefined>;
```


Whether the IPv6 is enabled for the distribution.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/cloudfront/distribution.ts#L116">property lastModifiedTime</a>
</h3>

```typescript
public lastModifiedTime: pulumi.Output<string>;
```


The date and time the distribution was last modified.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/cloudfront/distribution.ts#L122">property loggingConfig</a>
</h3>

```typescript
public loggingConfig: pulumi.Output<{ ... } | undefined>;
```


The [logging
configuration](#logging-config-arguments) that controls how logs are written
to your distribution (maximum one).

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/cloudfront/distribution.ts#L128">property orderedCacheBehaviors</a>
</h3>

```typescript
public orderedCacheBehaviors: pulumi.Output<{ ... }[] | undefined>;
```


An ordered list of [cache behaviors](#cache-behavior-arguments)
resource for this distribution. List from top to bottom
+    in order of precedence. The topmost cache behavior will have precedence 0.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/cloudfront/distribution.ts#L133">property origins</a>
</h3>

```typescript
public origins: pulumi.Output<{ ... }[]>;
```


One or more [origins](#origin-arguments) for this
distribution (multiples allowed).

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/cloudfront/distribution.ts#L138">property priceClass</a>
</h3>

```typescript
public priceClass: pulumi.Output<string | undefined>;
```


The price class for this distribution. One of
`PriceClass_All`, `PriceClass_200`, `PriceClass_100`

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/cloudfront/distribution.ts#L143">property restrictions</a>
</h3>

```typescript
public restrictions: pulumi.Output<{ ... }>;
```


The [restriction
configuration](#restrictions-arguments) for this distribution (maximum one).

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/cloudfront/distribution.ts#L149">property retainOnDelete</a>
</h3>

```typescript
public retainOnDelete: pulumi.Output<boolean | undefined>;
```


Disables the distribution instead of
deleting it when destroying the resource through Terraform. If this is set,
the distribution needs to be deleted manually afterwards. Default: `false`.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/cloudfront/distribution.ts#L155">property status</a>
</h3>

```typescript
public status: pulumi.Output<string>;
```


The current status of the distribution. `Deployed` if the
distribution's information is fully propagated throughout the Amazon
CloudFront system.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/cloudfront/distribution.ts#L159">property tags</a>
</h3>

```typescript
public tags: pulumi.Output<Tags | undefined>;
```


A mapping of tags to assign to the resource.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/node_modules/@pulumi/pulumi/resource.d.ts#L11">property urn</a>
</h3>

```typescript
urn: Output<URN>;
```


urn is the stable logical URN used to distinctly address a resource, both before and after
deployments.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/cloudfront/distribution.ts#L165">property viewerCertificate</a>
</h3>

```typescript
public viewerCertificate: pulumi.Output<{ ... }>;
```


The [SSL
configuration](#viewer-certificate-arguments) for this distribution (maximum
one).

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/cloudfront/distribution.ts#L171">property webAclId</a>
</h3>

```typescript
public webAclId: pulumi.Output<string | undefined>;
```


If you're using AWS WAF to filter CloudFront
requests, the Id of the AWS WAF web ACL that is associated with the
distribution.

<h2 class="pdoc-module-header" id="OriginAccessIdentity">
<a class="pdoc-member-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/cloudfront/originAccessIdentity.ts#L14">class OriginAccessIdentity</a>
</h2>

Creates an Amazon CloudFront origin access identity.

For information about CloudFront distributions, see the
[Amazon CloudFront Developer Guide][1]. For more information on generating
origin access identities, see
[Using an Origin Access Identity to Restrict Access to Your Amazon S3 Content][2].

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/cloudfront/originAccessIdentity.ts#L57">constructor</a>
</h3>

```typescript
new OriginAccessIdentity(name: string, args?: OriginAccessIdentityArgs, opts?: pulumi.CustomResourceOptions)
```


Create a OriginAccessIdentity resource with the given unique name, arguments, and options.

* `name` The _unique_ name of the resource.
* `args` The arguments to use to populate this resource&#39;s properties.
* `opts` A bag of options that control this resource&#39;s behavior.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/cloudfront/originAccessIdentity.ts#L23">method get</a>
</h3>

```typescript
public static get(name: string, id: pulumi.Input<pulumi.ID>, state?: OriginAccessIdentityState): OriginAccessIdentity
```


Get an existing OriginAccessIdentity resource's state with the given name, ID, and optional extra
properties used to qualify the lookup.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/node_modules/@pulumi/pulumi/resource.d.ts#L13">method getProvider</a>
</h3>

```typescript
getProvider(moduleMember: string): ProviderResource | undefined
```

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/node_modules/@pulumi/pulumi/resource.d.ts#L85">method isInstance</a>
</h3>

```typescript
static isInstance(obj: any): boolean
```


Returns true if the given object is an instance of CustomResource.  This is designed to work even when
multiple copies of the Pulumi SDK have been loaded into the same process.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/cloudfront/originAccessIdentity.ts#L31">property callerReference</a>
</h3>

```typescript
public callerReference: pulumi.Output<string>;
```


Internal value used by CloudFront to allow future
updates to the origin access identity.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/cloudfront/originAccessIdentity.ts#L36">property cloudfrontAccessIdentityPath</a>
</h3>

```typescript
public cloudfrontAccessIdentityPath: pulumi.Output<string>;
```


A shortcut to the full path for the
origin access identity to use in CloudFront, see below.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/cloudfront/originAccessIdentity.ts#L40">property comment</a>
</h3>

```typescript
public comment: pulumi.Output<string | undefined>;
```


An optional comment for the origin access identity.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/cloudfront/originAccessIdentity.ts#L45">property etag</a>
</h3>

```typescript
public etag: pulumi.Output<string>;
```


The current version of the origin access identity's information.
For example: `E2QWRUHAPOMQZL`.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/cloudfront/originAccessIdentity.ts#L51">property iamArn</a>
</h3>

```typescript
public iamArn: pulumi.Output<string>;
```


A pre-generated ARN for use in S3 bucket policies (see below).
Example: `arn:aws:iam::cloudfront:user/CloudFront Origin Access Identity
E2QWRUHAPOMQZL`.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/node_modules/@pulumi/pulumi/resource.d.ts#L80">property id</a>
</h3>

```typescript
id: Output<ID>;
```


id is the provider-assigned unique ID for this managed resource.  It is set during
deployments and may be missing (undefined) during planning phases.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/cloudfront/originAccessIdentity.ts#L57">property s3CanonicalUserId</a>
</h3>

```typescript
public s3CanonicalUserId: pulumi.Output<string>;
```


The Amazon S3 canonical user ID for the origin
access identity, which you use when giving the origin access identity read
permission to an object in Amazon S3.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/node_modules/@pulumi/pulumi/resource.d.ts#L11">property urn</a>
</h3>

```typescript
urn: Output<URN>;
```


urn is the stable logical URN used to distinctly address a resource, both before and after
deployments.

<h2 class="pdoc-module-header" id="DistributionArgs">
<a class="pdoc-member-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/cloudfront/distribution.ts#L408">interface DistributionArgs</a>
</h2>

The set of arguments for constructing a Distribution resource.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/cloudfront/distribution.ts#L413">property aliases</a>
</h3>

```typescript
aliases?: pulumi.Input<pulumi.Input<string>[]>;
```


Extra CNAMEs (alternate domain names), if any, for
this distribution.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/cloudfront/distribution.ts#L417">property cacheBehaviors</a>
</h3>

```typescript
cacheBehaviors?: pulumi.Input<pulumi.Input<{ ... }>[]>;
```


**Deprecated**, use `ordered_cache_behavior` instead.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/cloudfront/distribution.ts#L422">property comment</a>
</h3>

```typescript
comment?: pulumi.Input<string>;
```


Any comments you want to include about the
distribution.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/cloudfront/distribution.ts#L426">property customErrorResponses</a>
</h3>

```typescript
customErrorResponses?: pulumi.Input<pulumi.Input<{ ... }>[]>;
```


One or more [custom error response](#custom-error-response-arguments) elements (multiples allowed).

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/cloudfront/distribution.ts#L431">property defaultCacheBehavior</a>
</h3>

```typescript
defaultCacheBehavior: pulumi.Input<{ ... }>;
```


The [default cache behavior](#default-cache-behavior-arguments) for this distribution (maximum
one).

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/cloudfront/distribution.ts#L436">property defaultRootObject</a>
</h3>

```typescript
defaultRootObject?: pulumi.Input<string>;
```


The object that you want CloudFront to
return (for example, index.html) when an end user requests the root URL.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/cloudfront/distribution.ts#L441">property enabled</a>
</h3>

```typescript
enabled: pulumi.Input<boolean>;
```


Whether the distribution is enabled to accept end
user requests for content.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/cloudfront/distribution.ts#L447">property httpVersion</a>
</h3>

```typescript
httpVersion?: pulumi.Input<string>;
```


The maximum HTTP version to support on the
distribution. Allowed values are `http1.1` and `http2`. The default is
`http2`.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/cloudfront/distribution.ts#L451">property isIpv6Enabled</a>
</h3>

```typescript
isIpv6Enabled?: pulumi.Input<boolean>;
```


Whether the IPv6 is enabled for the distribution.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/cloudfront/distribution.ts#L457">property loggingConfig</a>
</h3>

```typescript
loggingConfig?: pulumi.Input<{ ... }>;
```


The [logging
configuration](#logging-config-arguments) that controls how logs are written
to your distribution (maximum one).

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/cloudfront/distribution.ts#L463">property orderedCacheBehaviors</a>
</h3>

```typescript
orderedCacheBehaviors?: pulumi.Input<pulumi.Input<{ ... }>[]>;
```


An ordered list of [cache behaviors](#cache-behavior-arguments)
resource for this distribution. List from top to bottom
+    in order of precedence. The topmost cache behavior will have precedence 0.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/cloudfront/distribution.ts#L468">property origins</a>
</h3>

```typescript
origins: pulumi.Input<pulumi.Input<{ ... }>[]>;
```


One or more [origins](#origin-arguments) for this
distribution (multiples allowed).

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/cloudfront/distribution.ts#L473">property priceClass</a>
</h3>

```typescript
priceClass?: pulumi.Input<string>;
```


The price class for this distribution. One of
`PriceClass_All`, `PriceClass_200`, `PriceClass_100`

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/cloudfront/distribution.ts#L478">property restrictions</a>
</h3>

```typescript
restrictions: pulumi.Input<{ ... }>;
```


The [restriction
configuration](#restrictions-arguments) for this distribution (maximum one).

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/cloudfront/distribution.ts#L484">property retainOnDelete</a>
</h3>

```typescript
retainOnDelete?: pulumi.Input<boolean>;
```


Disables the distribution instead of
deleting it when destroying the resource through Terraform. If this is set,
the distribution needs to be deleted manually afterwards. Default: `false`.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/cloudfront/distribution.ts#L488">property tags</a>
</h3>

```typescript
tags?: pulumi.Input<Tags>;
```


A mapping of tags to assign to the resource.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/cloudfront/distribution.ts#L494">property viewerCertificate</a>
</h3>

```typescript
viewerCertificate: pulumi.Input<{ ... }>;
```


The [SSL
configuration](#viewer-certificate-arguments) for this distribution (maximum
one).

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/cloudfront/distribution.ts#L500">property webAclId</a>
</h3>

```typescript
webAclId?: pulumi.Input<string>;
```


If you're using AWS WAF to filter CloudFront
requests, the Id of the AWS WAF web ACL that is associated with the
distribution.

<h2 class="pdoc-module-header" id="DistributionState">
<a class="pdoc-member-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/cloudfront/distribution.ts#L264">interface DistributionState</a>
</h2>

Input properties used for looking up and filtering Distribution resources.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/cloudfront/distribution.ts#L270">property activeTrustedSigners</a>
</h3>

```typescript
activeTrustedSigners?: pulumi.Input<{ ... }>;
```


The key pair IDs that CloudFront is aware of for
each trusted signer, if the distribution is set up to serve private content
with signed URLs.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/cloudfront/distribution.ts#L275">property aliases</a>
</h3>

```typescript
aliases?: pulumi.Input<pulumi.Input<string>[]>;
```


Extra CNAMEs (alternate domain names), if any, for
this distribution.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/cloudfront/distribution.ts#L279">property arn</a>
</h3>

```typescript
arn?: pulumi.Input<string>;
```


The ARN (Amazon Resource Name) for the distribution. For example: arn:aws:cloudfront::123456789012:distribution/EDFDVBD632BHDS5, where 123456789012 is your AWS account ID.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/cloudfront/distribution.ts#L283">property cacheBehaviors</a>
</h3>

```typescript
cacheBehaviors?: pulumi.Input<pulumi.Input<{ ... }>[]>;
```


**Deprecated**, use `ordered_cache_behavior` instead.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/cloudfront/distribution.ts#L288">property callerReference</a>
</h3>

```typescript
callerReference?: pulumi.Input<string>;
```


Internal value used by CloudFront to allow future
updates to the distribution configuration.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/cloudfront/distribution.ts#L293">property comment</a>
</h3>

```typescript
comment?: pulumi.Input<string>;
```


Any comments you want to include about the
distribution.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/cloudfront/distribution.ts#L297">property customErrorResponses</a>
</h3>

```typescript
customErrorResponses?: pulumi.Input<pulumi.Input<{ ... }>[]>;
```


One or more [custom error response](#custom-error-response-arguments) elements (multiples allowed).

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/cloudfront/distribution.ts#L302">property defaultCacheBehavior</a>
</h3>

```typescript
defaultCacheBehavior?: pulumi.Input<{ ... }>;
```


The [default cache behavior](#default-cache-behavior-arguments) for this distribution (maximum
one).

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/cloudfront/distribution.ts#L307">property defaultRootObject</a>
</h3>

```typescript
defaultRootObject?: pulumi.Input<string>;
```


The object that you want CloudFront to
return (for example, index.html) when an end user requests the root URL.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/cloudfront/distribution.ts#L312">property domainName</a>
</h3>

```typescript
domainName?: pulumi.Input<string>;
```


The DNS domain name of either the S3 bucket, or
web site of your custom origin.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/cloudfront/distribution.ts#L317">property enabled</a>
</h3>

```typescript
enabled?: pulumi.Input<boolean>;
```


Whether the distribution is enabled to accept end
user requests for content.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/cloudfront/distribution.ts#L322">property etag</a>
</h3>

```typescript
etag?: pulumi.Input<string>;
```


The current version of the distribution's information. For example:
`E2QWRUHAPOMQZL`.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/cloudfront/distribution.ts#L328">property hostedZoneId</a>
</h3>

```typescript
hostedZoneId?: pulumi.Input<string>;
```


The CloudFront Route 53 zone ID that can be used to
route an [Alias Resource Record Set][7] to. This attribute is simply an
alias for the zone ID `Z2FDTNDATAQYW2`.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/cloudfront/distribution.ts#L334">property httpVersion</a>
</h3>

```typescript
httpVersion?: pulumi.Input<string>;
```


The maximum HTTP version to support on the
distribution. Allowed values are `http1.1` and `http2`. The default is
`http2`.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/cloudfront/distribution.ts#L339">property inProgressValidationBatches</a>
</h3>

```typescript
inProgressValidationBatches?: pulumi.Input<number>;
```


The number of invalidation batches
currently in progress.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/cloudfront/distribution.ts#L343">property isIpv6Enabled</a>
</h3>

```typescript
isIpv6Enabled?: pulumi.Input<boolean>;
```


Whether the IPv6 is enabled for the distribution.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/cloudfront/distribution.ts#L347">property lastModifiedTime</a>
</h3>

```typescript
lastModifiedTime?: pulumi.Input<string>;
```


The date and time the distribution was last modified.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/cloudfront/distribution.ts#L353">property loggingConfig</a>
</h3>

```typescript
loggingConfig?: pulumi.Input<{ ... }>;
```


The [logging
configuration](#logging-config-arguments) that controls how logs are written
to your distribution (maximum one).

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/cloudfront/distribution.ts#L359">property orderedCacheBehaviors</a>
</h3>

```typescript
orderedCacheBehaviors?: pulumi.Input<pulumi.Input<{ ... }>[]>;
```


An ordered list of [cache behaviors](#cache-behavior-arguments)
resource for this distribution. List from top to bottom
+    in order of precedence. The topmost cache behavior will have precedence 0.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/cloudfront/distribution.ts#L364">property origins</a>
</h3>

```typescript
origins?: pulumi.Input<pulumi.Input<{ ... }>[]>;
```


One or more [origins](#origin-arguments) for this
distribution (multiples allowed).

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/cloudfront/distribution.ts#L369">property priceClass</a>
</h3>

```typescript
priceClass?: pulumi.Input<string>;
```


The price class for this distribution. One of
`PriceClass_All`, `PriceClass_200`, `PriceClass_100`

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/cloudfront/distribution.ts#L374">property restrictions</a>
</h3>

```typescript
restrictions?: pulumi.Input<{ ... }>;
```


The [restriction
configuration](#restrictions-arguments) for this distribution (maximum one).

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/cloudfront/distribution.ts#L380">property retainOnDelete</a>
</h3>

```typescript
retainOnDelete?: pulumi.Input<boolean>;
```


Disables the distribution instead of
deleting it when destroying the resource through Terraform. If this is set,
the distribution needs to be deleted manually afterwards. Default: `false`.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/cloudfront/distribution.ts#L386">property status</a>
</h3>

```typescript
status?: pulumi.Input<string>;
```


The current status of the distribution. `Deployed` if the
distribution's information is fully propagated throughout the Amazon
CloudFront system.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/cloudfront/distribution.ts#L390">property tags</a>
</h3>

```typescript
tags?: pulumi.Input<Tags>;
```


A mapping of tags to assign to the resource.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/cloudfront/distribution.ts#L396">property viewerCertificate</a>
</h3>

```typescript
viewerCertificate?: pulumi.Input<{ ... }>;
```


The [SSL
configuration](#viewer-certificate-arguments) for this distribution (maximum
one).

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/cloudfront/distribution.ts#L402">property webAclId</a>
</h3>

```typescript
webAclId?: pulumi.Input<string>;
```


If you're using AWS WAF to filter CloudFront
requests, the Id of the AWS WAF web ACL that is associated with the
distribution.

<h2 class="pdoc-module-header" id="OriginAccessIdentityArgs">
<a class="pdoc-member-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/cloudfront/originAccessIdentity.ts#L130">interface OriginAccessIdentityArgs</a>
</h2>

The set of arguments for constructing a OriginAccessIdentity resource.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/cloudfront/originAccessIdentity.ts#L134">property comment</a>
</h3>

```typescript
comment?: pulumi.Input<string>;
```


An optional comment for the origin access identity.

<h2 class="pdoc-module-header" id="OriginAccessIdentityState">
<a class="pdoc-member-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/cloudfront/originAccessIdentity.ts#L93">interface OriginAccessIdentityState</a>
</h2>

Input properties used for looking up and filtering OriginAccessIdentity resources.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/cloudfront/originAccessIdentity.ts#L98">property callerReference</a>
</h3>

```typescript
callerReference?: pulumi.Input<string>;
```


Internal value used by CloudFront to allow future
updates to the origin access identity.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/cloudfront/originAccessIdentity.ts#L103">property cloudfrontAccessIdentityPath</a>
</h3>

```typescript
cloudfrontAccessIdentityPath?: pulumi.Input<string>;
```


A shortcut to the full path for the
origin access identity to use in CloudFront, see below.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/cloudfront/originAccessIdentity.ts#L107">property comment</a>
</h3>

```typescript
comment?: pulumi.Input<string>;
```


An optional comment for the origin access identity.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/cloudfront/originAccessIdentity.ts#L112">property etag</a>
</h3>

```typescript
etag?: pulumi.Input<string>;
```


The current version of the origin access identity's information.
For example: `E2QWRUHAPOMQZL`.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/cloudfront/originAccessIdentity.ts#L118">property iamArn</a>
</h3>

```typescript
iamArn?: pulumi.Input<string>;
```


A pre-generated ARN for use in S3 bucket policies (see below).
Example: `arn:aws:iam::cloudfront:user/CloudFront Origin Access Identity
E2QWRUHAPOMQZL`.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/cloudfront/originAccessIdentity.ts#L124">property s3CanonicalUserId</a>
</h3>

```typescript
s3CanonicalUserId?: pulumi.Input<string>;
```


The Amazon S3 canonical user ID for the origin
access identity, which you use when giving the origin access identity read
permission to an object in Amazon S3.

