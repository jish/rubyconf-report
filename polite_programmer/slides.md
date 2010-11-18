!SLIDE subsection transition=scrollUp
# The Polite Programmer #
## Jim Weirich, Chris Nelson, Ed Sumerfield ##

!SLIDE transition=scrollUp
# Black Magic -- Method Missing #

    @@@ ruby
    class BlackMagic
      def method_missing(sym)
        if md = sym.to_s.match(/^play_(.*)/)
          play(md[1])
        end
      end
    end

    BlackMagic.new.play_song
    # => "playing song"

!SLIDE transition=scrollUp
# Gray Magic #

    @@@ ruby
    class GrayMagic < BlackMagic
      def method_missing(sym)
        if md = sym.to_s.match(/^watch_(.*)/)
          watch(md[1])
        end
      end
    end

    GrayMagic.new.watch_movie
    # => "watching movie"

!SLIDE
# Gray Magic #

    @@@ ruby
    class GrayMagic < BlackMagic
      def method_missing(sym)
        if md = sym.to_s.match(/^watch_(.*)/)
          watch(md[1])
        end
      end
    end

    GrayMagic.new.play_song
    # => ???


!SLIDE transition=scrollUp
# Gray Magic #

    @@@ ruby
    class GrayMagic < BlackMagic
      def method_missing(sym)
        if md = sym.to_s.match(/^watch_(.*)/)
          watch(md[1])
        else
          super
        end
      end
    end

    GrayMagic.new.play_song
    # => "playing song"

!SLIDE bullets transition=scrollUp
* implement `respond_to?`
* don't pollute namespaces
* _especially the global namespace_


