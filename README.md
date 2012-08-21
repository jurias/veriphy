Veriphy is a small, lightweight testing framework.

To use, copy the file Veriphy.php, and run a file or directory against it.

Ex:

Tests.php
------------------------------------------------
<?php
  
  test('1 equals 1', function() {
    $x = 1;
    verify($x)->is(1);
  });
  
  test('new array', function() {
    $x = array();
    
    test('is array', function() use ($x) {
      verify($x)->is_array();
    });
    
    test('is empty', function() use ($x) {
      verify($x)->is_empty();
    });
  });



And then run:
php Veriphy.php Tests.php