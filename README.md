# ansible-role-transmission-daemon

[![Build Status](https://travis-ci.org/linuxhq/ansible-role-transmission-daemon.svg?branch=master)](https://travis-ci.org/linuxhq/ansible-role-transmission-daemon)

RHEL/CentOS - A fast, easy, and free bittorrent client 

## Requirements

None

## Role Variables

Available variables are listed below, along with default values:

    td_alt_speed_down: 50
    td_alt_speed_enabled: False
    td_alt_speed_time_begin: 540
    td_alt_speed_time_day: 127
    td_alt_speed_time_enabled: False
    td_alt_speed_time_end: 1020
    td_alt_speed_up: 50
    td_bind_address_ipv4: '0.0.0.0'
    td_bind_address_ipv6: '::'
    td_blocklist_enabled: False
    td_blocklist_url: 'http://www.example.com/blocklist'
    td_cache_size_mb: 4
    td_dht_enabled: True
    td_download_dir: '/var/lib/transmission/Downloads'
    td_download_queue_enabled: True
    td_download_queue_size: 5
    td_encryption: 1
    td_idle_seeding_limit: 30
    td_idle_seeding_limit_enabled: False
    td_incomplete_dir: '/var/lib/transmission/Downloads'
    td_incomplete_dir_enabled: False
    td_lpd_enabled: False
    td_message_level: 1
    td_peer_congestion_algorithm: ''
    td_peer_id_ttl_hours: 6
    td_peer_limit_global: 200
    td_peer_limit_per_torrent: 50
    td_peer_port: 51413
    td_peer_port_random_high: 65535
    td_port_random_low: 49152
    td_peer_port_random_on_start: False
    td_peer_socket_tos: 'default'
    td_pex_enabled: True
    td_port_forwarding_enabled: True
    td_preallocation: 1
    td_prefetch_enabled: True
    td_queue_stalled_enabled: True
    td_queue_stalled_minutes: 30
    td_ratio_limit: 2
    td_ratio_limit_enabled: False
    td_rename_partial_files: True
    td_rpc_authentication_required: False
    td_rpc_bind_address: '0.0.0.0'
    td_rpc_enabled: True
    td_rpc_password: '{81c0bf5837de960f693ce3df337bc5f30dce6ebezuTWtlG8'
    td_rpc_port: 9091
    td_rpc_url: '/transmission/'
    td_rpc_username:
    td_rpc_whitelist: [ '127.0.0.1' ]
    td_rpc_whitelist_enabled: True
    td_scrape_paused_torrents_enabled: True
    td_script_torrent_done_enabled: False
    td_script_torrent_done_filename:
    td_seed_queue_enabled: False
    td_seed_queue_size: 10
    td_speed_limit_down: 100
    td_speed_limit_down_enabled: False
    td_speed_limit_up: 100
    td_speed_limit_up_enabled: False
    td_start_added_torrents: True
    td_trash_original_torrent_files: False
    td_umask: 18
    td_upload_slots_per_torrent: 14
    td_utp_enabled: True

By default, the transmission rpc password is 'transmission'

## Dependencies

 * https://galaxy.ansible.com/linuxhq/epel/

## Example Playbook

    - hosts: servers
      roles:
        - role: linuxhq.transmission-daemon
          td_blocklist_enabled: True
          td_blocklist_url: 'http://john.bitsurge.net/public/biglist.p2p.gz'
          td_dht_enabled: False
          td_pex_enabled: False
          td_rpc_whitelist: [ '127.0.0.1', '192.168.0.*' ]
          td_umask: 0

## License

BSD

## Author Information

This role was created by [Taylor Kimball](http://www.linuxhq.org).
