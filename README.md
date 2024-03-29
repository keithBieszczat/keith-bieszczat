# Optional list of the audience identifiers for the server the token was presented to.
# Audience-aware token authenticators (for example, OIDC token authenticators)
# should verify the token was intended for at least one of the audiences in this list,
# and return the intersection of this list and the valid audiences for the token in the response status.
# This ensures the token is valid to authenticate to the server it was presented to.
# If no audiences are provided, the token should be validated to authenticate to the Kubernetes API server.
"audiences": ["https://myserver.example.com", "https://myserver.internal.example.com"]

# API version to use when decoding the ExecCredentials resource. Required.
#
# The API version returned by the plugin MUST match the version listed here.
#
# To integrate with tools that support multiple versions (such as client.authentication.k8s.io/v1beta1),
# set an environment variable, pass an argument to the tool that indicates which version the exec plugin expects,
# or read the version from the ExecCredential object in the KUBERNETES_EXEC_INFO environment variable.
apiVersion: "client.authentication.k8s.io/v1"

# Environment variables to set when executing the plugin. Optional.
env:
- name: "FOO"
  value: "bar"

# Arguments to pass when executing the plugin. Optional.
args:
- "arg1"
- "arg2"

# Text shown to the user when the executable doesn't seem to be present. Optional.
installHint: |
  example-client-go-exec-plugin is required to authenticate
  to the current cluster.  It can be installed:

  On macOS: brew install example-client-go-exec-plugin

  On Ubuntu: apt-get install example-client-go-exec-plugin

  On Fedora: dnf install example-client-go-exec-plugin

  ...        

# Whether or not to provide cluster information, which could potentially contain
# very large CA data, to this exec plugin as a part of the KUBERNETES_EXEC_INFO
# environment variable.
provideClusterInfo: true

# The contract between the exec plugin and the standard input I/O stream. If the
# contract cannot be satisfied, this plugin will not be run and an error will be
# returned. Valid values are "Never" (this exec plugin never uses standard input),
# "IfAvailable" (this exec plugin wants to use standard input if it is available),
# or "Always" (this exec plugin requires standard input to function). Required.
interactiveMode: Never

File.fnmatch('cat',       'cat')        #=> true  # match entire string

// +listType=map

struct block_device     *s_bdev;
struct list_head        s_mounts;       /* vfsmount(s) of this one */
struct quota_mount_options s_dquot;     /* Diskquota specific options */
/* The next field is used by knfsd when converting a (inode number based)
 * file handle into a dentry. As it builds a path in the dcache tree from
 * the bottom up, there may for a time be a subpath of dentrys which is not * connected to the main tree.  This semaphore ensure that there is only ever * one such free path per filesystem.  Note that unconnected files (or other * non-directories) are allowed, but not unconnected diretories. */ struct semaphore s_nfsd_free_path_sem; };
name: mmosley user: auth-provider: config: client-id: kubernetes client-secret: 1db158f6-177d-4d9c-8a8b-d36869918ec5 id-token: eyJraWQiOiJDTj1vaWRjaWRwLnRyZW1vbG8ubGFuLCBPVT1EZW1vLCBPPVRybWVvbG8gU2VjdXJpdHksIEw9QXJsaW5ndG9uLCBTVD1WaXJnaW5pYSwgQz1VUy1DTj1rdWJlLWNhLTEyMDIxNDc5MjEwMzYwNzMyMTUyIiwiYWxnIjoiUlMyNTYifQ.eyJpc3MiOiJodHRwczovL29pZGNpZHAudHJlbW9sby5sYW46ODQ0My9hdXRoL2lkcC9PaWRjSWRQIiwiYXVkIjoia3ViZXJuZXRlcyIsImV4cCI6MTQ4MzU0OTUxMSwianRpIjoiMm96US15TXdFcHV4WDlHZUhQdy1hZyIsImlhdCI6MTQ4MzU0OTQ1MSwibmJmIjoxNDgzNTQ5MzMxLCJzdWIiOiI0YWViMzdiYS1iNjQ1LTQ4ZmQtYWIzMC0xYTAxZWU0MWUyMTgifQ.w6p4J_6qQ1HzTG9nrEOrubxIMb9K5hzcMPxc9IxPx2K4xO9l-oFiUw93daH3m5pluP6K7eOE6txBuRVfEcpJSwlelsOsW8gb8VJcnzMS9EnZpeA0tW_p-mnkFc3VcfyXuhe5R3G7aa5d8uHv70yJ9Y3-UhjiN9EhpMdfPAoEB9fYKKkJRzF7utTTIPGrSaSU6d2pcpfYKaxIwePzEkT4DfcQthoZdy9ucNvvLoi1DIC-UocFD8HLs8LYKEqSxQvOcvnThbObJ9af71EwmuE21fO5KzMW20KtAeget1gnldOosPtz1G5EwvaQ401-RPQzPGMVBld0_zMCAwZttJ4knw idp-certificate-authority: /root/ca.pem idp-issuer-url: https://oidcidp.tremolo.lan:8443/auth/idp/OidcIdP refresh-token: q1bKLFOyUiosTfawzA93TzZIDzH2TNa2SMm0zEiPKTUwME6BkEo6Sql5yUWVBSWpKUGphaWpxSVAfekBOZbBhaEW+VlFUeVRGcluyVF5JT4+haZmPsluFoFu5XkpXk5BXqkubectl --token=eyJhbGciOiJSUzI1NiJ9.eyJpc3MiOiJodHRwczovL21sYi50cmVtb2xvLmxhbjo4MDQzL2F1dGgvaWRwL29pZGMiLCJhdWQiOiJrdWJlcm5ldGVzIiwiZXhwIjoxNDc0NTk2NjY5LCJqdGkiOiI2RDUzNXoxUEpFNjJOR3QxaWVyYm9RIiwiaWF0IjoxNDc0NTk2MzY5LCJuYmYiOjE0NzQ1OTYyNDksInN1YiI6Im13aW5kdSIsInVzZXJfcm9sZSI6WyJ1c2VycyIsIm5ldy1uYW1lc3BhY2Utdmlld2VyIl0sImVtYWlsIjoibXdpbmR1QG5vbW9yZWplZGkuY29tIn0.f2As579n9VNoaKzoF-dOQGmXkFKf1FMyNV0-va_B63jn-_n9LGSCca_6IVMP8pO-Zb4KvRqGyTP0r3HkHxYy5c81AnIh8ijarruczl-TK_yF5akjSTHFZD-0gRzlevBDiH8Q79NAr-ky0P4iIXS8lY9Vnjch5MF74Zx0c3alKJHJUnnpjIACByfF2SCaYzbWFMUNat-K1PaUk5-ujMBG7yYnr95xD-63n8CO8teGUAAEMx6zRjzfhnhbzX-ajwZLGwGUBT4WqjMs70-6a7_8gZmLZb2az1cZynkFRj2BaCkVT3A2RrjeEwZEtGXlMqKJ1_I2ulrOVsYx01_yD35-rw get nodes Webhook Token Authentication


// +listMapKey=type
// +patchStrategy=merge
// +patchMergeKey=type
// +optional
Conditions []metav1.Condition json:"conditions,omitempty" patchStrategy:"merge" patchMergeKey:"type" protobuf:"bytes,1,rep,name=conditions”
// type of condition in CamelCase or in foo.example.com/CamelCase.
// +required
Type string json:"type" protobuf:"bytes,1,opt,name=type"
// status of the condition, one of True, False, Unknown.
// +required
Status ConditionStatus json:"status" protobuf:"bytes,2,opt,name=status"
// observedGeneration represents the .metadata.generation that the condition was set based upon.
// For instance, if .metadata.generation is currently 12, but the .status.conditions[x].observedGeneration is 9, the condition is out of date
// with respect to the current state of the instance.
// +optional
ObservedGeneration int64 json:"observedGeneration,omitempty" protobuf:"varint,3,opt,name=observedGeneration"
// lastTransitionTime is the last time the condition transitioned from one status to another.
// This should be when the underlying condition changed. If that is not known, then using the time when the API field changed is acceptable.
// +required
LastTransitionTime Time json:"lastTransitionTime" protobuf:"bytes,4,opt,name=lastTransitionTime"
// reason contains a programmatic identifier indicating the reason for the condition's last transition.
// Producers of specific condition types may define expected values and meanings for this field,
// and whether the values are considered a guaranteed API.
// The value should be a CamelCase string.
// This field may not be empty.
// +required
Reason string json:"reason" protobuf:"bytes,5,opt,name=reason"
// message is a human readable message indicating details about the transition.
// This may be an empty string.
// +required
Message string json:"message" protobuf:"bytes,6,opt,name=message”
ports:

name: www
containerPort: 80
ports:
www:
containerPort: 80
Client #1 Client #2
GET Foo GET Foo
Set Foo.Bar = "one" Set Foo.Baz = "two"
PUT Foo PUT Foo

for a single resource, the suffix should be Ref, with the field name

providing an indication as to the resource type referenced.

secretRef:
name: foo
# namespace would generally not be needed and is discouraged,
# as explained above.
namespace: foo-namespace

guidance for the field name is the same as a single resource.

fooRef:
group: sns.services.k8s.aws
resource: topics
name: foo
namespace: foo-namespace

fooRef:
group: sns.services.k8s.aws
kind: Topic
name: foo
namespace: foo-namespace
fooObjectRef:
group: operator.openshift.io
resource: openshiftapiservers
name: cluster
# namespace is unset if the resource is cluster-scoped, or lives in the
# same namespace as the referrer.

fooFieldRef:
version: v1 # version of the resource

group is elided in the ConfigMap example, since it has a blank group in the OpenAPI spec.

resource: configmaps
fieldPath: data.foo
/apis/{group}/{version}/{resource}/

$ curl -v -k -H "Authorization: Bearer WhCDvq4VPpYhrcfmF6ei7V9qlbqTubUc" https://10.240.122.184:443/api/v1/namespaces/default/pods/grafana

GET /api/v1/namespaces/default/pods/grafana HTTP/1.1
User-Agent: curl/7.26.0
Host: 10.240.122.184
Accept: /
Authorization: Bearer WhCDvq4VPpYhrcfmF6ei7V9qlbqTubUc
< HTTP/1.1 404 Not Found
< Content-Type: application/json
< Date: Wed, 20 May 2015 18:10:42 GMT
< Content-Length: 232
<
{
"kind": "Status",
"apiVersion": "v1",
"metadata": {},
"status": "Failure",
"message": "pods "grafana" not found",
"reason": "NotFound",
"details": {
"name": "grafana",
"kind": "pods"
},
"code": 404
}
kubectl get --raw "/api/v1/nodes/minikube/proxy/stats/summary”
apiVersion: v1
kind: Secret
metadata:

Name MUST be of form "bootstrap-token-"

name: bootstrap-token-07401b
namespace: kube-system

Type MUST be 'bootstrap.kubernetes.io/token'

type: bootstrap.kubernetes.io/token
stringData:

Human readable description. Optional.

description: "The default bootstrap token generated by 'kubeadm init'."

Token ID and secret. Required.

token-id: 07401b
token-secret: f395accd246ae52d

Expiration. Optional.

expiration: 2017-03-10T03:22:11Z

Allowed usages.

usage-bootstrap-authentication: "true"
usage-bootstrap-signing: "true"

Extra groups to authenticate the token as. Must start with "system:bootstrappers:"

auth-extra-groups: system:bootstrappers:worker,system:bootstrappers:ingress

{
  "targets": [
    {
      "target_name": "addon",
      "sources": [ "addon.cc" ]
    }
  ]
} COPY
In cases where there is more than one .cc file, simply add the additional filename to the sources array:

"sources": ["addon.cc", "myexample.cc"] COPY
Once the binding.gyp file is ready, the example addons can be configured and built using node-gyp:

node-gyp configure build // addon.cc
#include <node.h>

namespace demo {

using v8::Exception;
using v8::FunctionCallbackInfo;
using v8::Isolate;
using v8::Local;
using v8::Number;
using v8::Object;
using v8::String;
using v8::Value;

// This is the implementation of the "add" method
// Input arguments are passed using the
// const FunctionCallbackInfo<Value>& args struct
void Add(const FunctionCallbackInfo<Value>& args) {
  Isolate* isolate = args.GetIsolate();

  // Check the number of arguments passed.
  if (args.Length() < 2) {
    // Throw an Error that is passed back to JavaScript
    isolate->ThrowException(Exception::TypeError(
        String::NewFromUtf8(isolate,
                            "Wrong number of arguments").ToLocalChecked()));
    return;
  }

  // Check the argument types
  if (!args[0]->IsNumber() || !args[1]->IsNumber()) {
    isolate->ThrowException(Exception::TypeError(
        String::NewFromUtf8(isolate,
                            "Wrong arguments").ToLocalChecked()));
    return;
  }

  // Perform the operation
  double value =
      args[0].As<Number>()->Value() + args[1].As<Number>()->Value();
  Local<Number> num = Number::New(isolate, value);

  // Set the return value (using the passed in
  // FunctionCallbackInfo<Value>&)
  args.GetReturnValue().Set(num);
}

void Init(Local<Object> exports) {
  NODE_SET_METHOD(exports, "add", Add);
}

NODE_MODULE(NODE_GYP_MODULE_NAME, Init)

}  // namespace demo COPY
Once compiled, the example addon can be required and used from within Node.js:

// test.js
const addon = require('./build/Release/addon');

console.log('This should be eight:', addon.add(3, 5)); COPY
Callbacks#

It is common practice within addons to pass JavaScript functions to a C++ function and execute them from there. The following example illustrates how to invoke such callbacks:

// addon.cc
#include <node.h>

namespace demo {

using v8::Context;
using v8::Function;
using v8::FunctionCallbackInfo;
using v8::Isolate;
using v8::Local;
using v8::Null;
using v8::Object;
using v8::String;
using v8::Value;

void RunCallback(const FunctionCallbackInfo<Value>& args) {
  Isolate* isolate = args.GetIsolate();
  Local<Context> context = isolate->GetCurrentContext();
  Local<Function> cb = Local<Function>::Cast(args[0]);
  const unsigned argc = 1;
  Local<Value> argv[argc] = {
      String::NewFromUtf8(isolate,
                          "hello world").ToLocalChecked() };
  cb->Call(context, Null(isolate), argc, argv).ToLocalChecked();
}

void Init(Local<Object> exports, Local<Object> module) {
  NODE_SET_METHOD(module, "exports", RunCallback);
}

NODE_MODULE(NODE_GYP_MODULE_NAME, Init)

}  // namespace demo COPY
This example uses a two-argument form of Init() that receives the full module object as the second argument. This allows the addon to completely overwrite exports with a single function instead of adding the function as a property of exports.

To test it, run the following JavaScript:

// test.js
const addon = require('./build/Release/addon');

addon((msg) => {
  console.log(msg);
// Prints: 'hello world'
}); COPY
In this example, the callback function is invoked synchronously.

Object factory#

Addons can create and return new objects from within a C++ function as illustrated in the following example. An object is created and returned with a property msg that echoes the string passed to createObject():

// addon.cc
#include <node.h>

namespace demo {

using v8::Context;
using v8::FunctionCallbackInfo;
using v8::Isolate;
using v8::Local;
using v8::Object;
using v8::String;
using v8::Value;

void CreateObject(const FunctionCallbackInfo<Value>& args) {
  Isolate* isolate = args.GetIsolate();
  Local<Context> context = isolate->GetCurrentContext();

  Local<Object> obj = Object::New(isolate);
  obj->Set(context,
           String::NewFromUtf8(isolate,
                               "msg").ToLocalChecked(),
                               args[0]->ToString(context).ToLocalChecked())
           .FromJust();

  args.GetReturnValue().Set(obj);
}

void Init(Local<Object> exports, Local<Object> module) {
  NODE_SET_METHOD(module, "exports", CreateObject);
}

NODE_MODULE(NODE_GYP_MODULE_NAME, Init)

}  // namespace demo COPY
To test it in JavaScript:

// test.js
const addon = require('./build/Release/addon');

const obj1 = addon('hello');
const obj2 = addon('world');
console.log(obj1.msg, obj2.msg);
// Prints: 'hello world' COPY
Function factory#

Another common scenario is creating JavaScript functions that wrap C++ functions and returning those back to JavaScript:

// addon.cc
#include <node.h>

namespace demo {

using v8::Context;
using v8::Function;
using v8::FunctionCallbackInfo;
using v8::FunctionTemplate;
using v8::Isolate;
using v8::Local;
using v8::Object;
using v8::String;
using v8::Value;

void MyFunction(const FunctionCallbackInfo<Value>& args) {
  Isolate* isolate = args.GetIsolate();
  args.GetReturnValue().Set(String::NewFromUtf8(
      isolate, "hello world").ToLocalChecked());
}

void CreateFunction(const FunctionCallbackInfo<Value>& args) {
  Isolate* isolate = args.GetIsolate();

  Local<Context> context = isolate->GetCurrentContext();
  Local<FunctionTemplate> tpl = FunctionTemplate::New(isolate, MyFunction);
  Local<Function> fn = tpl->GetFunction(context).ToLocalChecked();

  // omit this to make it anonymous
  fn->SetName(String::NewFromUtf8(
      isolate, "theFunction").ToLocalChecked());

  args.GetReturnValue().Set(fn);
}

void Init(Local<Object> exports, Local<Object> module) {
  NODE_SET_METHOD(module, "exports", CreateFunction);
}

NODE_MODULE(NODE_GYP_MODULE_NAME, Init)

}  // namespace demo COPY
To test:

// test.js
const addon = require('./build/Release/addon');

const fn = addon();
console.log(fn());
// Prints: 'hello world' COPY
Wrapping C++ objects#

It is also possible to wrap C++ objects/classes in a way that allows new instances to be created using the JavaScript new operator:

// addon.cc
#include <node.h>
#include "myobject.h"

namespace demo {

using v8::Local;
using v8::Object;

void InitAll(Local<Object> exports) {
  MyObject::Init(exports);
}

NODE_MODULE(NODE_GYP_MODULE_NAME, InitAll)

}  // namespace demo COPY
Then, in myobject.h, the wrapper class inherits from node::ObjectWrap:

// myobject.h
#ifndef MYOBJECT_H
#define MYOBJECT_H

#include <node.h>
#include <node_object_wrap.h>

namespace demo {

class MyObject : public node::ObjectWrap {
 public:
  static void Init(v8::Local<v8::Object> exports);

 private:
  explicit MyObject(double value = 0);
  ~MyObject();

  static void New(const v8::FunctionCallbackInfo<v8::Value>& args);
  static void PlusOne(const v8::FunctionCallbackInfo<v8::Value>& args);

  double value_;
};

}  // namespace demo

#endif COPY
In myobject.cc, implement the various methods that are to be exposed. Below, the method plusOne() is exposed by adding it to the constructor's prototype:

// myobject.cc
#include "myobject.h"

namespace demo {

using v8::Context;
using v8::Function;
using v8::FunctionCallbackInfo;
using v8::FunctionTemplate;
using v8::Isolate;
using v8::Local;
using v8::Number;
using v8::Object;
using v8::ObjectTemplate;
using v8::String;
using v8::Value;

MyObject::MyObject(double value) : value_(value) {
}

MyObject::~MyObject() {
}

void MyObject::Init(Local<Object> exports) {
  Isolate* isolate = exports->GetIsolate();
  Local<Context> context = isolate->GetCurrentContext();

  Local<ObjectTemplate> addon_data_tpl = ObjectTemplate::New(isolate);
  addon_data_tpl->SetInternalFieldCount(1);  // 1 field for the MyObject::New()
  Local<Object> addon_data =
      addon_data_tpl->NewInstance(context).ToLocalChecked();

  // Prepare constructor template
  Local<FunctionTemplate> tpl = FunctionTemplate::New(isolate, New, addon_data);
  tpl->SetClassName(String::NewFromUtf8(isolate, "MyObject").ToLocalChecked());
  tpl->InstanceTemplate()->SetInternalFieldCount(1);

  // Prototype
  NODE_SET_PROTOTYPE_METHOD(tpl, "plusOne", PlusOne);

  Local<Function> constructor = tpl->GetFunction(context).ToLocalChecked();
  addon_data->SetInternalField(0, constructor);
  exports->Set(context, String::NewFromUtf8(
      isolate, "MyObject").ToLocalChecked(),
      constructor).FromJust();
}

void MyObject::New(const FunctionCallbackInfo<Value>& args) {
  Isolate* isolate = args.GetIsolate();
  Local<Context> context = isolate->GetCurrentContext();

  if (args.IsConstructCall()) {
    // Invoked as constructor: `new MyObject(...)`
    double value = args[0]->IsUndefined() ?
        0 : args[0]->NumberValue(context).FromMaybe(0);
    MyObject* obj = new MyObject(value);
    obj->Wrap(args.This());
    args.GetReturnValue().Set(args.This());
  } else {
    // Invoked as plain function `MyObject(...)`, turn into construct call.
    const int argc = 1;
    Local<Value> argv[argc] = { args[0] };
    Local<Function> cons =
        args.Data().As<Object>()->GetInternalField(0)
            .As<Value>().As<Function>();
    Local<Object> result =
        cons->NewInstance(context, argc, argv).ToLocalChecked();
    args.GetReturnValue().Set(result);
  }
}

void MyObject::PlusOne(const FunctionCallbackInfo<Value>& args) {
  Isolate* isolate = args.GetIsolate();

  MyObject* obj = ObjectWrap::Unwrap<MyObject>(args.Holder());
  obj->value_ += 1;

  args.GetReturnValue().Set(Number::New(isolate, obj->value_));
}

}  // namespace demo COPY
To build this example, the myobject.cc file must be added to the binding.gyp:

{
  "targets": [
    {
      "target_name": "addon",
      "sources": [
        "addon.cc",
        "myobject.cc"
      ]
    }
  ]
} COPY
Test it with:

// test.js
const addon = require('./build/Release/addon');

const obj = new addon.MyObject(10);
console.log(obj.plusOne());
// Prints: 11
console.log(obj.plusOne());
// Prints: 12
console.log(obj.plusOne());
// Prints: 13 COPY
The destructor for a wrapper object will run when the object is garbage-collected. For destructor testing, there are command-line flags that can be used to make it possible to force garbage collection. These flags are provided by the underlying V8 JavaScript engine. They are subject to change or removal at any time. They are not documented by Node.js or V8, and they should never be used outside of testing.

During shutdown of the process or worker threads destructors are not called by the JS engine. Therefore it's the responsibility of the user to track these objects and ensure proper destruction to avoid resource leaks.

Factory of wrapped objects#

Alternatively, it is possible to use a factory pattern to avoid explicitly creating object instances using the JavaScript new operator:

const obj = addon.createObject();
// instead of:
// const obj = new addon.Object(); COPY
First, the createObject() method is implemented in addon.cc:

// addon.cc
#include <node.h>
#include "myobject.h"

namespace demo {

using v8::FunctionCallbackInfo;
using v8::Isolate;
using v8::Local;
using v8::Object;
using v8::String;
using v8::Value;

void CreateObject(const FunctionCallbackInfo<Value>& args) {
  MyObject::NewInstance(args);
}

void InitAll(Local<Object> exports, Local<Object> module) {
  MyObject::Init(exports->GetIsolate());

  NODE_SET_METHOD(module, "exports", CreateObject);
}

NODE_MODULE(NODE_GYP_MODULE_NAME, InitAll)

}  // namespace demo COPY
In myobject.h, the static method NewInstance() is added to handle instantiating the object. This method takes the place of using new in JavaScript:

// myobject.h
#ifndef MYOBJECT_H
#define MYOBJECT_H

#include <node.h>
#include <node_object_wrap.h>

namespace demo {

class MyObject : public node::ObjectWrap {
 public:
  static void Init(v8::Isolate* isolate);
  static void NewInstance(const v8::FunctionCallbackInfo<v8::Value>& args);

 private:
  explicit MyObject(double value = 0);
  ~MyObject();

  static void New(const v8::FunctionCallbackInfo<v8::Value>& args);
  static void PlusOne(const v8::FunctionCallbackInfo<v8::Value>& args);
  static v8::Global<v8::Function> constructor;
  double value_;
};

}  // namespace demo

#endif COPY
The implementation in myobject.cc is similar to the previous example:

// myobject.cc
#include <node.h>
#include "myobject.h"

namespace demo {

using node::AddEnvironmentCleanupHook;
using v8::Context;
using v8::Function;
using v8::FunctionCallbackInfo;
using v8::FunctionTemplate;
using v8::Global;
using v8::Isolate;
using v8::Local;
using v8::Number;
using v8::Object;
using v8::String;
using v8::Value;

// Warning! This is not thread-safe, this addon cannot be used for worker
// threads.
Global<Function> MyObject::constructor;

MyObject::MyObject(double value) : value_(value) {
}

MyObject::~MyObject() {
}

void MyObject::Init(Isolate* isolate) {
  // Prepare constructor template
  Local<FunctionTemplate> tpl = FunctionTemplate::New(isolate, New);
  tpl->SetClassName(String::NewFromUtf8(isolate, "MyObject").ToLocalChecked());
  tpl->InstanceTemplate()->SetInternalFieldCount(1);

  // Prototype
  NODE_SET_PROTOTYPE_METHOD(tpl, "plusOne", PlusOne);

  Local<Context> context = isolate->GetCurrentContext();
  constructor.Reset(isolate, tpl->GetFunction(context).ToLocalChecked());

  AddEnvironmentCleanupHook(isolate, [](void*) {
    constructor.Reset();
  }, nullptr);
}

void MyObject::New(const FunctionCallbackInfo<Value>& args) {
  Isolate* isolate = args.GetIsolate();
  Local<Context> context = isolate->GetCurrentContext();

  if (args.IsConstructCall()) {
    // Invoked as constructor: `new MyObject(...)`
    double value = args[0]->IsUndefined() ?
        0 : args[0]->NumberValue(context).FromMaybe(0);
    MyObject* obj = new MyObject(value);
    obj->Wrap(args.This());
    args.GetReturnValue().Set(args.This());
  } else {
    // Invoked as plain function `MyObject(...)`, turn into construct call.
    const int argc = 1;
    Local<Value> argv[argc] = { args[0] };
    Local<Function> cons = Local<Function>::New(isolate, constructor);
    Local<Object> instance =
        cons->NewInstance(context, argc, argv).ToLocalChecked();
    args.GetReturnValue().Set(instance);
  }
}

void MyObject::NewInstance(const FunctionCallbackInfo<Value>& args) {
  Isolate* isolate = args.GetIsolate();

  const unsigned argc = 1;
  Local<Value> argv[argc] = { args[0] };
  Local<Function> cons = Local<Function>::New(isolate, constructor);
  Local<Context> context = isolate->GetCurrentContext();
  Local<Object> instance =
      cons->NewInstance(context, argc, argv).ToLocalChecked();

  args.GetReturnValue().Set(instance);
}

void MyObject::PlusOne(const FunctionCallbackInfo<Value>& args) {
  Isolate* isolate = args.GetIsolate();

  MyObject* obj = ObjectWrap::Unwrap<MyObject>(args.Holder());
  obj->value_ += 1;

  args.GetReturnValue().Set(Number::New(isolate, obj->value_));
}

}  // namespace demo COPY
Once again, to build this example, the myobject.cc file must be added to the binding.gyp:

{
  "targets": [
    {
      "target_name": "addon",
      "sources": [
        "addon.cc",
        "myobject.cc"
      ]
    }
  ]
} COPY
Test it with:

// test.js
const createObject = require('./build/Release/addon');

const obj = createObject(10);
console.log(obj.plusOne());
// Prints: 11
console.log(obj.plusOne());
// Prints: 12
console.log(obj.plusOne());
// Prints: 13

const obj2 = createObject(20);
console.log(obj2.plusOne());
// Prints: 21
console.log(obj2.plusOne());
// Prints: 22
console.log(obj2.plusOne());
// Prints: 23 COPY
Passing wrapped objects around#

In addition to wrapping and returning C++ objects, it is possible to pass wrapped objects around by unwrapping them with the Node.js helper function node::ObjectWrap::Unwrap. The following examples shows a function add() that can take two MyObject objects as input arguments:

// addon.cc
#include <node.h>
#include <node_object_wrap.h>
#include "myobject.h"

namespace demo {

using v8::Context;
using v8::FunctionCallbackInfo;
using v8::Isolate;
using v8::Local;
using v8::Number;
using v8::Object;
using v8::String;
using v8::Value;

void CreateObject(const FunctionCallbackInfo<Value>& args) {
  MyObject::NewInstance(args);
}

void Add(const FunctionCallbackInfo<Value>& args) {
  Isolate* isolate = args.GetIsolate();
  Local<Context> context = isolate->GetCurrentContext();

  MyObject* obj1 = node::ObjectWrap::Unwrap<MyObject>(
      args[0]->ToObject(context).ToLocalChecked());
  MyObject* obj2 = node::ObjectWrap::Unwrap<MyObject>(
      args[1]->ToObject(context).ToLocalChecked());

  double sum = obj1->value() + obj2->value();
  args.GetReturnValue().Set(Number::New(isolate, sum));
}

void InitAll(Local<Object> exports) {
  MyObject::Init(exports->GetIsolate());

  NODE_SET_METHOD(exports, "createObject", CreateObject);
  NODE_SET_METHOD(exports, "add", Add);
}

NODE_MODULE(NODE_GYP_MODULE_NAME, InitAll)

}  // namespace demo COPY
In myobject.h, a new public method is added to allow access to private values after unwrapping the object.

// myobject.h
#ifndef MYOBJECT_H
#define MYOBJECT_H

#include <node.h>
#include <node_object_wrap.h>

namespace demo {

class MyObject : public node::ObjectWrap {
 public:
  static void Init(v8::Isolate* isolate);
  static void NewInstance(const v8::FunctionCallbackInfo<v8::Value>& args);
  inline double value() const { return value_; }

 private:
  explicit MyObject(double value = 0);
  ~MyObject();

  static void New(const v8::FunctionCallbackInfo<v8::Value>& args);
  static v8::Global<v8::Function> constructor;
  double value_;
};

}  // namespace demo

#endif COPY
The implementation of myobject.cc is similar to before:

// myobject.cc
#include <node.h>
#include "myobject.h"

namespace demo {

using node::AddEnvironmentCleanupHook;
using v8::Context;
using v8::Function;
using v8::FunctionCallbackInfo;
using v8::FunctionTemplate;
using v8::Global;
using v8::Isolate;
using v8::Local;
using v8::Object;
using v8::String;
using v8::Value;

// Warning! This is not thread-safe, this addon cannot be used for worker
// threads.
Global<Function> MyObject::constructor;

MyObject::MyObject(double value) : value_(value) {
}

MyObject::~MyObject() {
}

void MyObject::Init(Isolate* isolate) {
  // Prepare constructor template
  Local<FunctionTemplate> tpl = FunctionTemplate::New(isolate, New);
  tpl->SetClassName(String::NewFromUtf8(isolate, "MyObject").ToLocalChecked());
  tpl->InstanceTemplate()->SetInternalFieldCount(1);

  Local<Context> context = isolate->GetCurrentContext();
  constructor.Reset(isolate, tpl->GetFunction(context).ToLocalChecked());

  AddEnvironmentCleanupHook(isolate, [](void*) {
    constructor.Reset();
  }, nullptr);
}

void MyObject::New(const FunctionCallbackInfo<Value>& args) {
  Isolate* isolate = args.GetIsolate();
  Local<Context> context = isolate->GetCurrentContext();

  if (args.IsConstructCall()) {
    // Invoked as constructor: `new MyObject(...)`
    double value = args[0]->IsUndefined() ?
        0 : args[0]->NumberValue(context).FromMaybe(0);
    MyObject* obj = new MyObject(value);
    obj->Wrap(args.This());
    args.GetReturnValue().Set(args.This());
  } else {
    // Invoked as plain function `MyObject(...)`, turn into construct call.
    const int argc = 1;
    Local<Value> argv[argc] = { args[0] };
    Local<Function> cons = Local<Function>::New(isolate, constructor);
    Local<Object> instance =
        cons->NewInstance(context, argc, argv).ToLocalChecked();
    args.GetReturnValue().Set(instance);
  }
}

void MyObject::NewInstance(const FunctionCallbackInfo<Value>& args) {
  Isolate* isolate = args.GetIsolate();

  const unsigned argc = 1;
  Local<Value> argv[argc] = { args[0] };
  Local<Function> cons = Local<Function>::New(isolate, constructor);
  Local<Context> context = isolate->GetCurrentContext();
  Local<Object> instance =
      cons->NewInstance(context, argc, argv).ToLocalChecked();

  args.GetReturnValue().Set(instance);
}

}  // namespace demo COPY
Test it with:

// test.js
const addon = require('./build/Release/addon');

const obj1 = addon.createObject(10);
const obj2 = addon.createObject(20);
const result = addon.add(obj1, obj2);

console.log(result);
// Prints: 30 
// hello.cc using Node-API
#include <node_api.h>

namespace demo {

napi_value Method(napi_env env, napi_callback_info args) {
  napi_value greeting;
  napi_status status;

  status = napi_create_string_utf8(env, "world", NAPI_AUTO_LENGTH, &greeting);
  if (status != napi_ok) return nullptr;
  return greeting;
}

napi_value init(napi_env env, napi_value exports) {
  napi_status status;
  napi_value fn;

  status = napi_create_function(env, nullptr, 0, Method, nullptr, &fn);
  if (status != napi_ok) return nullptr;

  status = napi_set_named_property(env, exports, "hello", fn);
  if (status != napi_ok) return nullptr;
  return exports;
}

NAPI_MODULE(NODE_GYP_MODULE_NAME, init)

}  // namespace demotry {
  return require('./build/Release/addon.node');
} catch (err) {
  return require('./build/Debug/addon.node');
}


{
  "targets": [
    {
      "target_name": "addon",
      "sources": [ "hello.cc" ]
    }
  ]
}
// hello.js
const addon = require('./build/Release/addon');

console.log(addon.hello());
// Prints: 'world'


PORT=3000 ruby FILE_NAME
npm install express
// You installed the `express` library earlier. For more information, see "[JavaScript example: Install dependencies](#javascript-example-install-dependencies)."
const express = require('express');

// This initializes a new Express application.
const app = express();

// This defines a POST route at the `/webhook` path. This path matches the path that you specified for the smee.io forwarding. For more information, see "[Forward webhooks](#forward-webhooks)."
//
// Once you deploy your code to a server and update your webhook URL, you should change this to match the path portion of the URL for your webhook.
app.post('/webhook', express.json({type: 'application/json'}), (request, response) => {

  // Respond to indicate that the delivery was successfully received.
  // Your server should respond with a 2XX response within 10 seconds of receiving a webhook delivery. If your server takes longer than that to respond, then GitHub terminates the connection and considers the delivery a failure.
  response.status(202).send('Accepted');

  // Check the `x-github-event` header to learn what event type was sent.
  const githubEvent = request.headers['x-github-event'];

  // You should add logic to handle each event type that your webhook is subscribed to.
  // For example, this code handles the `issues` and `ping` events.
  //
  // If any events have an `action` field, you should also add logic to handle each action that you are interested in.
  // For example, this code handles the `opened` and `closed` actions for the `issue` event.
  //
  // For more information about the data that you can expect for each event type, see "[AUTOTITLE](/webhooks/webhook-events-and-payloads)."
  if (githubEvent === 'issues') {
    const data = request.body;
    const action = data.action;
    if (action === 'opened') {
      console.log(`An issue was opened with this title: ${data.issue.title}`);
    } else if (action === 'closed') {
      console.log(`An issue was closed by ${data.issue.user.login}`);
    } else {
      console.log(`Unhandled action for the issue event: ${action}`);
    }
  } else if (githubEvent === 'ping') {
    console.log('GitHub sent the ping event');
  } else {
    console.log(`Unhandled event: ${githubEvent}`);
  }
});

// This defines the port where your server should listen.
// 3000 matches the port that you specified for webhook forwarding. For more information, see "[Forward webhooks](#forward-webhooks)."
//
// Once you deploy your code to a server, you should change this to match the port where your server is listening.
const port = 3000;

// This starts the server and tells it to listen at the specified port.
app.listen(port, () => {
  console.log(`Server is running on port ${port}`);
});
node FILE_NAME
[npm install --global smee-client
smee --url WEBHOOK_PROXY_URL --path /webhook --port 3000
Forwarding WEBHOOK_PROXY_URL to http://127.0.0.1:3000/webhook
Connected WEBHOOK_PROXY_URL
gem install bundler
bundle init
bundle install
bundle add sinatra
# These are the dependencies for this code. You installed the `sinatra` gem earlier. For more information, see "[Ruby example: Install dependencies](#ruby-example-install-dependencies)." The `json` library is a standard Ruby library, so you don't need to install it.
require 'sinatra'
require 'json'

# The `/webhook` route matches the path that you specified for the smee.io forwarding. For more information, see "[Forward webhooks](#forward-webhooks)."
#
# Once you deploy your code to a server and update your webhook URL, you should change this to match the path portion of the URL for your webhook.
post '/webhook' do

  # Respond to indicate that the delivery was successfully received.
  # Your server should respond with a 2XX response within 10 seconds of receiving a webhook delivery. If your server takes longer than that to respond, then GitHub terminates the connection and considers the delivery a failure.
  status 202

  # Check the `X-GitHub-Event` header to learn what event type was sent.
  # Sinatra changes `X-GitHub-Event` to `HTTP_X_GITHUB_EVENT`.
  github_event = request.env['HTTP_X_GITHUB_EVENT']

  # You should add logic to handle each event type that your webhook is subscribed to.
  # For example, this code handles the `issues` and `ping` events.
  #
  # If any events have an `action` field, you should also add logic to handle each action that you are interested in.
  # For example, this code handles the `opened` and `closed` actions for the `issue` event.
  #
  # For more information about the data that you can expect for each event type, see "[AUTOTITLE](/webhooks/webhook-events-and-payloads)."
  if github_event == "issues"
    data = JSON.parse(request.body.read)
    action = data['action']
    if action == "opened"
      puts "An issue was opened with this title: #{data['issue']['title']}"
    elsif action == "closed"
      puts "An issue was closed by #{data['issue']['user']['login']}"
    else
      puts "Unhandled action for the issue event: #{action}"
    end
  elsif github_event == "ping"
    puts "GitHub sent the ping event"
  else
    puts "Unhandled event: #{github_event}"
  end
end
](https://github.com/keithBieszczat/Men-In-Black-Agency.git)https://github.com/keithBieszczat/Men-In-Black-Agency.git

git@github.com:keithBieszczat/Men-In-Black-Agency.git
echo "# Men-In-Black-Agency" >> README.md
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin git@github.com:keithBieszczat/Men-In-Black-Agency.git
git push -u origin main

git remote add origin git@github.com:keithBieszczat/Men-In-Black-Agency.git
git branch -M main
git push -u origin main


# keith-bieszczat
