!SLIDE subsection transition=scrollUp
# Mustache in the front, Mustache in the rear
## Patrick Ewing

!SLIDE transition=scrollUp
# speed
## Rendering tweets accounted for 12% of Twitters cpu usage

!SLIDE bullets transition=scrollUp
* haml
* mustache.rb
* erb
* jQuery ui
* mustache.js

!SLIDE transition=scrollUp

    @@@ javascript
    API.User.find('foo')
      .timeline()
      .first(20)
      .each(function(tweet) {
        new View.TweetView(tweet).toHtml;
    });

!SLIDE transition=scrollUp

    @@@ javascript
    twttr.view('foo')
      .superclass(twttr.views.BaseAPI)
      .methods({
        is_top_tweet: function() {
          return this.category === 'popular';
        }
    );

    class Stream Tweet < Views::Base
      def is_top_tweet
        category == 'popular'
      end
    end
