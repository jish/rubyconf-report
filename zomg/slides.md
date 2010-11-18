!SLIDE subsection transition=scrollUp
# ZOMG WHY IS THIS CODE SO SLOW? #
## Aaron Patterson ##

!SLIDE transition=scrollUp
# ActiveRecord 5x slower than Rails 2.3.5 #

!SLIDE bullets transition=scrollUp
# Rewrite #
# vs. #
# Superficial improvements #

!SLIDE transition=scrollUp
    lambda { ... }

    # vs

    class Callable
      def call; ... end
    end

!SLIDE center transition=scrollUp
![lambda_vs_method](lambda_vs_method.png)

!SLIDE transition=scrollUp
    class Foo
      def foo; end
      define_method :bar do; end
      class_eval %{ def baz; end }
    end

!SLIDE center transition=scrollUp
![define_method](define_method.png)

!SLIDE transition=scrollUp
    @list.map(&:to_i)

    # vs

    @list.map { |x| x.to_i }

!SLIDE center transition=scrollUp
![sym_to_proc](sym_to_proc.png)

!SLIDE bullets transition=scrollUp
# Rewrite #
# vs. #
# Superficial improvements #

!SLIDE center transition=scrollUp
![linked_list](linked_list.png)

!SLIDE center transition=scrollUp
![arels_big_o](arels_big_o.png)

!SLIDE center transition=scrollUp
![superficial](superficial.png)
