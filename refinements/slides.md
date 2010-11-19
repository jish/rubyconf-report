!SLIDE subsection transition=scrollUp
# Ruby 2.0
## Matz

!SLIDE transition=scrollUp
# keyword arguments

!SLIDE transition=scrollUp

    @@@ ruby
    def step(by: step, to: limit)
      ...
    end

    1.step(by: 2, to: 20) do |i|
      puts i
    end

!SLIDE center transition=scrollUp
# refinements

!SLIDE transition=scrollUp

    @@@ ruby
    class Foo
      def method
        "method"
      end
    end

    Foo.new.method # => "method"

!SLIDE transition=scrollUp

    @@@ ruby
    module Namespace
      refine Foo do
        def method
          "refined method"
        end
      end
    end

!SLIDE transition=scrollUp

    @@@ ruby
    module Closure
      using Namespace
      Foo.new.method # => "refined method"
    end

    Foo.new.method # => "method"

!SLIDE center transition=scrollUp
# Rite
## Ruby lite
