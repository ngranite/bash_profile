## DB can be reached from bastion
`ssh -L <local_port_above_1024>:<remote_db_hostname_or_ip>:<remote_db_port> username@bastion`

Now, just connect to DB as if its running on localhost as `localhost:<local_port_above_1024>`

## Have one more hop? (`bastion <-> server1 <-> db:3306`)
`ssh -L <local_port_above_1024>:<db_hostname_or_ip>:<db_port> username@server1 -J username@bastion`

Now, just connect to DB as if its running on localhost as `localhost:<local_port_above_1024>`
