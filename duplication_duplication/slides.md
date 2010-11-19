!SLIDE subsection transition=scrollUp
# Duplication
# Duplication
## David Chelimsky
## David Chelimsky

!SLIDE transition=scrollUp
# DRY

!SLIDE transition=scrollUp
# DRY
## does not mean _"don't type the same characters twice"_
## it is about isolation of change

!SLIDE transition=scrollUp

    @@@ ruby
    "/year/2002/month/04/day/30"
    "/year/2004/month/01/day/12"
    "/year/2007/month/09/day/24"

!SLIDE transition=scrollUp

    @@@ ruby
    YEAR = 'year'
    MONTH = 'month'
    DAY = 'day'

    "/#{YEAR}/2002/#{MONTH}/04/#{DAY}/30"
    "/#{YEAR}/2004/#{MONTH}/01/#{DAY}/12"
    "/#{YEAR}/2007/#{MONTH}/09/#{DAY}/24"

!SLIDE transition=scrollUp

    @@@ ruby
    class Line
      attr_accessor :start_point,
        :end_point,
        :length # duplication of length
    end

!SLIDE transition=scrollUp
# every piece of knowledge should have a single unambiguous authoratative representation

!SLIDE transition=scrollUp
# every time you reduce duplication you increase dependency
