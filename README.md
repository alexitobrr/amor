/***** Corazones grandes cayendo en tu blog *****/
if (typeof jQuery == 'undefined') {
  var script = document.createElement('script');
  script.type = 'text/javascript';
  script.src = 'http://ajax.googleapis.com/ajax/libs/jquery/1.7.1/jquery.min.js';
  script.onload = function() {
    var $pdj = jQuery.noConflict();
    initializeHearts($pdj);
  };
  document.head.appendChild(script);
} else {
  var $pdj = jQuery.noConflict();
  initializeHearts($pdj);
}

function initializeHearts($pdj) {
  $pdj(document).ready(function () {
    var c = $pdj(window).width();
    var d = $pdj(window).height();
    var e = function (a, b) {
      return Math.round(a + (Math.random() * (b - a)));
    };
    var f = function (a) {
      setTimeout(function () {
        a.css({ left: e(0, c) + 'px', top: '-30px', display: 'block', opacity: '0.' + e(10, 100) }).animate({ top: (d - 10) + 'px' }, e(8500, 10000), function () {
          $pdj(this).fadeOut('slow', function () {
            f(a);
          });
        });
      }, e(1, 9000));
    };
    $pdj('<div></div>').attr('id', 'corazonDiv').css({ position: 'fixed', width: (c - 20) + 'px', height: '1px', left: '0px', top: '-5px', display: 'block' }).appendTo('body');
    for (var i = 1; i <= 15; i++) {
      var g = $pdj('<img/>').attr('src', image_urls['corazon']).css({ position: 'absolute', left: e(0, c) + 'px', top: '-30px', display: 'block', opacity: '0.' + e(10, 100), 'margin-left': 0 }).addClass('corazonDrop').appendTo('#corazonDiv');
      f(g);
      g = null;
    }
    var h = 0;
    var j = 0;
    $pdj(window).resize(function () {
      c = $pdj(window).width();
      d = $pdj(window).height();
    });
  });
}
if (!image_urls) {
  var image_urls = Array();
}
if (!flash_urls) {
  var flash_urls = Array();
}
image_urls['corazon'] = "https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhUpShk9o_F_cdxYKkop8C1EcAcwyDh5J-wEXLXgSKjbjdnQTgu1Fp_MxSuXlv04X5viMn-i54V1I1hENhxLcBBpWeHa7vdbnjU8rFLRMTu9WmSoQpn8IJH5dYgfUcWg0DkHlw_z-a5PXU/s32/heart.png";
$pdj(document).ready(function () {
  var c = $pdj(window).width();
  var d = $pdj(window).height();
  var e = function (a, b) {
    return Math.round(a + (Math.random() * (b - a)));
  };
  var f = function (a) {
    setTimeout(function () {
      a.css({ left: e(0, c) + 'px', top: '-30px', display: 'block', opacity: '0.' + e(10, 100) }).animate({ top: (d - 10) + 'px' }, e(8500, 10000), function () {
        $pdj(this).fadeOut('slow', function () {
          f(a);
        });
      });
    }, e(1, 9000));
  };
  $pdj('<div></div>').attr('id', 'corazonDiv').css({ position: 'fixed', width: (c - 20) + 'px', height: '1px', left: '0px', top: '-5px', display: 'block' }).appendTo('body');
  for (var i = 1; i <= 15; i++) {
    var g = $pdj('<img/>').attr('src', image_urls['corazon']).css({ position: 'absolute', left: e(0, c) + 'px', top: '-30px', display: 'block', opacity: '0.' + e(10, 100), 'margin-left': 0 }).addClass('corazonDrop').appendTo('#corazonDiv');
    f(g);
    g = null;
  }
  var h = 0;
  var j = 0;
  $pdj(window).resize(function () {
    c = $pdj(window).width();
    d = $pdj(window).height();
  });
});
