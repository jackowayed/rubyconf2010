!SLIDE

# Mirah #

!SLIDE bullets incremental

* Charles Nutter
* JVM language
* Ruby-like syntax
* Statically-typed
* No runtime dependencies

!SLIDE

# Hello World #

    @@@ruby
    @name = "world"
    puts "Hello, #{@name}!"

!SLIDE

# Fibonacci #

    @@@ruby
    def fib(a:fixnum)
      if a < 2
        a
      else
        fib(a - 1) + fib(a - 2)
      end
    end
