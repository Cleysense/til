# Sort associate array by date
Example
```PHP
$arr = [
  [
    'id' => 12,
    'create_date' => '2019-02-26 06:38:31.915'
  ],
  [
    'id' => 19,
    'create_date' => '2019-03-04 10:28:21.849'
  ],
  [
    'id' => 32,
    'create_date' => '2019-03-10 10:39:40.601'
  ],
];

usort( $arr, function ( $a, $b )
{
  $a_date = new Datetime( $a['create_date'] );
  $b_date = new Datetime( $b['create_date'] );

  if ( $a_date === $b_date ) {
    return 0;
  }

  return ( $a_date > $b_date ) ? - 1 : 1;
} );
```