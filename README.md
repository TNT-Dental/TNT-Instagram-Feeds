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
      /*template: '<a href="{{link}}" target="_blank" class="item {{orientation}} {{type}}"><img src="{{image}}" /><div class="caption">{{caption}}</div></a>',*/
      template: '<div><a href="{{link}}" target="_blank" class="item {{orientation}} {{type}}"><img src="{{image}}" /></a></div>',
      target: "ig-feed",
      sortBy: "most-recent",
      after: function() {
        $("#ig-feed .video").parent().remove();       
        $("#ig-feed").slick({          
          centerMode:false,
          slidesToShow:5,          
          arrows:false,
          dots:false,
          autoplay:true,
          infinite:true,
          autoplaySpeed:0,
          speed:10000          
        });
      }
    }).run(); 
  }
});
```

## Links
[Codepen Example 1](https://codepen.io/endeart/pen/YboWLv)
