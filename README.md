# simple Equalize Height

## Usage
Use this code if you need to equalize height for a set of elements

```
<script type="text/javascript">
  (function( $ ){
      'use strict';
      
      $.fn.equalizeHeight = function () {
      
        var tallestHeight = 0,
            $panels = this;
        
        
        $panels.each(function(i, el){
          var elHeight = $(el).outerHeight();
          
          $(el).find('h2').html('Real high is: ' + elHeight + 'px');
          
          if (elHeight > tallestHeight) {
            tallestHeight = elHeight;
          }
        });
        
        $panels.css('min-height', tallestHeight);        
        return this;
      };
      
  }( jQuery ));
  
  
  $(document).ready(function () {
    'use strict';
    $('.part1').find('.panel').equalizeHeight();
    $('.part2').find('.panel').equalizeHeight();

  });
</script> 
```
## Demo

[Demo](https://benfarhat.github.io/jquery-equalize-height/)

2017 🖥 Benfarhat Elyes
