# TNT-Instagram-Feeds
Instagram feed rotations.

## Initializer [Slick Slider]
```javascript
$(function() {
  //Instagram feed rotation
  if($("#insta")) {
    new Instafeed({
      get: "user",
      userId: 236174443,
      accessToken: "236174443.1677ed0.51797b9db5994b6e97253ba65596df6d",
      resolution: "standard_resolution",
      useHttp: "true",
      limit: 10,    
      template: '<div><a href="{{link}}" target="_blank" class="item {{orientation}} {{type}}"><img src="{{image}}" /></a></div>',
      target: "ig-feed",
      sortBy: "most-recent",
      after: function() {
        $("#ig-feed .video").parent().remove();       
        $("#ig-feed").slick({          
          centerMode: true,
            slidesToShow: 5,
            arrows: false,
            infinite: true,
            autoplay: true,
            cssEase: 'linear',
            autoplaySpeed: 0,
            speed: 10000,
            responsive: [
                {
                    breakpoint: 980,
                    settings: {
                        slidesToShow: 4
                    }
                },
                {
                    breakpoint: 700,
                    settings: {
                        slidesToShow: 3
                    }
                },
                {
                    breakpoint: 400,
                    settings: {
                        slidesToShow: 2
                    }
                }]          
        });
      }
    }).run(); 
  }
});
```

## Instagram Accsess Token
1. Use clients Instagram Logins (Must be provided by GL or PM) if not, ask if they want to use a temporary feed.
2. Log in to their account and open a new browser tab.
3. While logged in, and on the same browser, go to https://instagram.pixelunion.net/
4. Click on Generate Access Token and "Authorize".

### Token Example
- 4000981380.1677ed0.cf5d5c68b6134a648a26b5bc2bd8b429
- First section before the [dot] is the account ID: 4000981380

## Links
[Codepen Example 1](https://codepen.io/endeart/pen/YboWLv)
