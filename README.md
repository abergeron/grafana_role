Role Name
=========

Role to install Grafana tools (Loki and Tempo for now)


Role Variables
--------------

  - grafana_install_{loki,tempo}: Defaults to false, set to true to
    install the component

  - grafana_{loki,tempo}_local_path: Defaults to "/data/{loki,tempo}",
    path to store permanent local data

  - grafana_{loki,tempo}_cert_{file,key}: HTTPS certficate to use for
    the service. If not specified, a self-signed certificate will be
    generated.

  - grafana_loki_log_retention: duration, time to keep log entries (0s
    means forever)

  - grafana_tempo_block_retention: duration, time to keep traces


Example Playbook
----------------

    - hosts: servers
      roles:
         - { role: abergeron.grafana, grafana_install_loki: true }

License
-------

BSD
