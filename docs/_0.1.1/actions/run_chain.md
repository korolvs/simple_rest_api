---
type: '0.1.1'
category: Actions
title: run_chain
description: Executes each method in a chain one by one
github: https://github.com/korolvs/resting_pug/blob/master/lib/resting_pug/actions.rb#L168
order: 6
---

## Description
Executes each method in a chain one by one

## Params
- [Array] **chain** - array of methods to execute

## Used in
- [#create]({{ site.baseurl }}/0.1.1/actions/create)
- [#update]({{ site.baseurl }}/0.1.1/actions/update)
- [#destroy]({{ site.baseurl }}/0.1.1/actions/destroy)
- [#show]({{ site.baseurl }}/0.1.1/actions/show)
- [#index]({{ site.baseurl }}/0.1.1/actions/index)

## Source code
```ruby
# lib/resting_pug/actions.rb

def run_chain(chain)
  chain.each do |action|
    self.send(action)
  end
end
```



