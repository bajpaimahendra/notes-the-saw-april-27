#### caching 

$cacheKey = md5(serialize($search_datas));
$this->load->driver('cache');
if ( ! $search_result = $this->cache->file->get($cacheKey)){
    $ping = PingRequest($search_id);
    //echo 'Total time in ping : ' . round( (microtime(true) - $time1) ).' seconds <br>';

    $time1 = microtime(true); 
    $search_result = amadeus_search($search_datas, $search_id);
    // Save into the cache for 5 minutes
    $this->cache->file->save($cacheKey, $search_result, 300);
}

var isFlightSearchData = '<?php  ?>';


function getCurrentTime(){
    var ct = new Date(); 
    ct.toUTCString();
    //e.setMinutes(e.getMinutes() + 10); // time after 10 min.
    //alert(e);
    return ct;
    
}

getFlightTimer();
load_flights

