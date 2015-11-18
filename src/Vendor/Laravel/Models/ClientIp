<?php

namespace PragmaRX\Tracker\Vendor\Laravel\Models;

class ClientIp extends Base
{

    protected $table = 'tracker_client_ips';

    protected $fillable = array(
        'client_ip',
        'geoip_id',
    );

    public function geoIp()
    {
        return $this->belongsTo($this->getConfig()->get('geoip_model'), 'geoip_id');
    }

    public function sessions()
    {
        return $this->hasMany($this->getConfig()->get('session_model'));
    }
}
