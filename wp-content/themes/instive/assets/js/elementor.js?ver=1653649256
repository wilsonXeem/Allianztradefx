(function ($, elementor) {
    "use strict";

    var Instive = {

        init: function () {

            var widgets = {
               
                'instive-main-slider.default': Instive.Main_Slider,
                'instive-content-slider.default': Instive.Content_Slider,
                'instive-testimonial.default': Instive.Testimonial,
                'instive-team-slider.default': Instive.Team,
                'instive-post-slider.default': Instive.Post_Slider,
                'instive-insurance.default': Instive.instive_insurance,
            };
            $.each(widgets, function (widget, callback) {
                elementor.hooks.addAction('frontend/element_ready/' + widget, callback);
            });

        },
        
        Main_Slider: function ($scope) {

         var $container = $scope.find('.main-slider');

         var controls= JSON.parse($container.attr('data-controls'));
              
         var navShow = Boolean(controls.show_nav?true:false);
         var autoslide = Boolean(controls.auto_nav_slide?true:false);
         var dot_nav_show = Boolean(controls.dot_nav_show?true:false);
         var ts_slider_speed = parseInt(controls.ts_slider_speed);
         
         if ($container.length > 0) {
            $container.owlCarousel({
               items: 1,
               loop: true,
               autoplay: autoslide,
               nav: navShow,
               dots: dot_nav_show,
               autoplayTimeout: ts_slider_speed,
               autoplayHoverPause: true,
               mouseDrag: false,
               smartSpeed: 1100,
               navText: ['<i class="icon icon-left-arrow2">', '<i class="icon icon-right-arrow2">'],
               responsive: {
                  0: {
                     items: 1,
                     nav: false,
                  },
                  600: {
                     items: 1,
                     nav: false,
                  },
                  1000: {
                     nav: navShow,
                  }
               }
         
            });
         }
     },


   // content slider 
  Content_Slider: function ($scope) {
      var $container = $scope.find('.content-slider');
      var controls_data = $container.attr('data-controls');

      var autoslide = false;
      var navShow = true;
      var dot_nav_show = true;
         if(controls_data){
            var controls= JSON.parse($container.attr('data-controls'));
            var navShow = Boolean(controls.show_nav?true:false);
            var autoslide = Boolean(controls.auto_nav_slide?true:false);
            var dot_nav_show = Boolean(controls.dot_nav_show?true:false);
         }
    
      
      if ($container.length > 0) {
         $container.owlCarousel({
            items: 1,
            loop: true,
            autoplay: autoslide,
            nav: navShow,
            dots: dot_nav_show,
            autoplayHoverPause: true,
            mouseDrag: false,
            smartSpeed: 1100,
            animateOut: 'fadeOut',
            navText: ['<i class="icon icon-left-arrow2">', '<i class="icon icon-right-arrow2">'],
          });
      }
   },
     Post_Slider: function ($scope) {

         var $container = $scope.find('.blog-post');

         var controls= JSON.parse($container.attr('data-controls'));
              
         var navShow = Boolean(controls.show_nav?true:false);
         var autoslide = Boolean(controls.auto_nav_slide?true:false);
         var dot_nav_show = Boolean(controls.dot_nav_show?true:false);
         var ts_slider_speed = parseInt(controls.ts_slider_speed);
         
         if ($container.length > 0) {
            $container.owlCarousel({
               items: 2,
               loop: true,
               autoplay: autoslide,
               nav: navShow,
               dots: dot_nav_show,
               autoplayTimeout: ts_slider_speed,
               autoplayHoverPause: true,
               mouseDrag: false,
               smartSpeed: 1100,
               navText: ['<i class="icon icon-left-arrow2">', '<i class="icon icon-right-arrow2">'],
               responsive: {
                  0: {
                     items: 1,
                     nav: false,
                  },
                  600: {
                     items: 1,
                     nav: false,
                  },
                  1000: {
                     items: 2,
                     nav: navShow,
                  }
               }
         
            });
         }
        
   
     },

     instive_insurance: function ($scope) {

         var $container = $scope.find('.ts-service-slider');

         var controls_data = $container.attr('data-controls');

         var autoslide = false;
         var slide_count = '4';
         var dot_nav_show = true;
            if(controls_data){
               var controls= JSON.parse($container.attr('data-controls'));
               var dot_nav_show = Boolean(controls.dot_nav_show?true:false);
               var slide_count = parseInt(controls.item_count);
            }

         if ($container.length > 0) {
            $container.owlCarousel({
               items: slide_count,
               loop: true,
               autoplay: autoslide,
               dots: dot_nav_show,
               autoplayHoverPause: true,
               mouseDrag: true,
               smartSpeed: 1100,
              
               responsive: {
                  0: {
                     items: 1,
                     nav: false,
                  },
                  600: {
                     items: 2,
                     nav: false,
                  },
                  768: {
                     items: 3,
                  },
                  1000: {
                     items: slide_count,
                  }
               }
         
            });
         }
        
   
     },

     Testimonial: function ($scope) {

      var $container = $scope.find('.ts-testimonial-sync1');

      if ($('.testimonial-slider').length > 0) {
         var testimonial = $scope.find('.testimonial-slider');
         testimonial.owlCarousel({
            items: 1,
            mouseDrag: true,
            loop: true,
            touchDrag: true,
            autoplay:false,
            dots: true,
            center: true,
            autoplayTimeout: 5000,
            margin:0,
            autoplayHoverPause: true,
            smartSpeed: 1000,
         });
        
      }
      if ($('.ts-testimonial-slider').length > 0) {
         var testimonial = $scope.find('.ts-testimonial-slider');
         testimonial.owlCarousel({
            items: 5,
            mouseDrag: true,
            loop: true,
            touchDrag: true,
            autoplay:false,
            dots: true,
            center: true,
            autoplayTimeout: 5000,
            margin:0,
            autoplayHoverPause: true,
            smartSpeed: 1000,
            responsive: {
               0: {
                  items: 3,
               },
               600: {
                  items: 3,
               },
               1000: {
                  items: 5,
               }
            }
      
         });
        
      }

      if ($('.ts-testimonial-slider-three').length > 0) {
       
         var testimonialSlider = $scope.find('.ts-testimonial-slider-three');
         var owl = testimonialSlider.owlCarousel({
            items 	 : 1,
            center	   : true, 
            nav        : false,
            dots       : true,
            loop       : false,
            margin     : 10,
            dotsContainer: '.testimonial-controls',
            navText: ['<i class="fas fa-arrow-right"></i>','<i class="fas fa-arrow-left"></i>'],
         });
      
         $('.testimonial-thumb').on('click', 'li', function(e) {
            owl.trigger('to.owl.carousel', [$(this).index(), 300]);
         });  
        
      }
      
     },
      
      Team: function ($scope){
            var $container = $scope.find('.ts-team-slider');
            var controls= JSON.parse($container.attr('data-controls'));
             
            var navShow = Boolean(controls.show_nav?true:false);
            var autoslide = Boolean(controls.auto_nav_slide?true:false);
            var dot_nav_show = Boolean(controls.dot_nav_show?true:false);
            var ts_slider_speed = parseInt(controls.ts_slider_speed);

            if ($('.ts-team-slider').length > 0) {
                var testimonial = $scope.find('.ts-team-slider');
                testimonial.owlCarousel({
                    items: 4,
                    mouseDrag: true,
                    loop: true,
                    touchDrag: true,
                    nav: navShow,
                    navText: ['<i class="icon icon-left-arrow2">', '<i class="icon icon-right-arrow2">'],
                    autoplay:autoslide,
                    dots: dot_nav_show,
                    autoplayTimeout: ts_slider_speed,
                    autoplayHoverPause: true,
                    smartSpeed: 1000,
                    responsive: {
                     0: {
                        items: 1,
                        nav: false,
                     },
                     600: {
                        items: 2,
                        nav: false,
                     },
                     1000: {
                        nav: navShow,
                     }
                  }
                });
                
            }
      },
      
    };
    $(window).on('elementor/frontend/init', Instive.init);
}(jQuery, window.elementorFrontend));


