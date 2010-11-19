!SLIDE subsection transition=scrollUp
# So You Think You Can Code?
## Aaron Patterson, Evan Phoenix, Rein Henrichs, Yossef Mendelssohn, John Barnette, Ben Bleything

!SLIDE transition=scrollUp
# Editors
## panel says: vi

!SLIDE transition=scrollUp
# indent private methods?
## panel says: no

!SLIDE transition=scrollUp
# Line length
## panel says: humans read better
## when lines are shorter
## 72 - 80


!SLIDE transition=scrollUp
# Ternary truthiness

    @@@ ruby
    def method
      @attribute ? true : false
    end

!SLIDE transition=scrollUp
# The bang bang

    @@@ ruby
    def method
      !!@attribute
    end

!SLIDE transition=scrollUp
# Feature envy

    @@@ ruby
    class Class
      def method
        klass = Klass.new(length, width)
        klass.length * klass.width
      end
    end
