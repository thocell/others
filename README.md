# others
<?php
function article_inarray_tag($tagnum)
{
    $atagarrbytag = array($tagnum);
    $atagarr      = array(
        pow(2, 0),
        pow(2, 1),
        pow(2, 2),
        pow(2, 3),
        pow(2, 4),
        pow(2, 5),
        pow(2, 6),
        pow(2, 7)
    );
    $k            = array_search($tagnum, $atagarr);
    for ($j = 0; $j < 8; $j++) {
        if ($j != $k) {
            for ($i = $j; $i < 8; $i++) {
                if ($i != $k) {
                    $tagnum += pow(2, $i);
                    $atagarrbytag[] = $tagnum;
                }
            }
               $tagnum = $atagarr[$k];
        }
    }
    return $atagarrbytag;
}
$atagarrbytag = article_inarray_tag(1);
print_r($atagarrbytag);
?>
