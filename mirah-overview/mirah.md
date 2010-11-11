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

!SLIDE small

# mirahc --java fib.mirah #

    // Generated from fib.mirah
    public class Fib extends java.lang.Object {
      public static void main(java.lang.String[] argv) {
      }
      public static int fib(int a) {
        // normally one line
        return (a < 2) ? (a) :
        ((Fib.fib((a - 1)) + Fib.fib((a - 2))));
      }
    }
