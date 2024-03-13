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
