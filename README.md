# README

## Steps to send an email

```ruby
require 'trycourier'

courier_api_key = ENV['COURIER_API_TEST_KEY']
client = Courier::Client.new courier_api_key
res = client.send({
  event: 'HHTPGNFB8TM6T3MYXSQKRKM7JNRK',
  recipient: 'f394d723-ca03-47ed-acaf-57d7327d31ad',
  profile: {
  },
  data: {
    ref: 'James Dean',
    firstname: 'Julia'
  },
})

puts res.code # the HTTP response code
puts res.message_id # if 200, this will be the Courier message ID for this notification
```
