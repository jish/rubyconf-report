!SLIDE subsection transition=scrollUp
# Ruby 2.0
## Matz

!SLIDE center transition=scrollUp
# refinements

!SLIDE transition=scrollUp

    @@@ ruby
    module Foo
      def method
        "method"
      end
    end

    Foo.method # => "method"

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
      Foo.method # => "refined method"
    end

    Foo.method # => "method"

!SLIDE transition=scrollUp

    @@@ ruby
    module Whatever
      include Namespace
    end

!SLIDE center transition=scrollUp
# Rite
## Ruby lite
