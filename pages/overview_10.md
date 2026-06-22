# require / require_relative

```ruby
# a.rb
class A
  def hello
    puts "hello"
  end
end
```

```ruby
# b.rb
require_relative "a"
A.new.hello
```

```bash
$ ./spinel b.rb
b.rb -> b
```
