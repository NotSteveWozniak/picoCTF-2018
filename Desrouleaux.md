#PicoCTF 2018
###Desrouleaux
I was able to solve the first 2 parts of this challenge fairly easily.  I will not cover those, as they have been thoroughly covered by others.  Instead this only deals with the third part of the Desrouleaux challenge:

**What is the number of unique destination ips a file is sent, on average? Needs to be correct to 2 decimal places.**

I had not idea what was being asked.  I stared at the data, **incidents.json**, for several minutes, but could not understand what was being asked.  I turned to Google, and found out I was not alone.  I found several write ups on how to brute force the solution.  While that worked, I wanted to try to figure this out.  It took about three hours, but I finally came up with something that mad sense to me and earned the flag.  This may or may not make sense to you.

This was the contents of **incidents.json** at the time I solved this challenge:
` 
{
    "tickets": [
        {
            "ticket_id": 0,
            "timestamp": "2016/09/21 20:53:04",
            "file_hash": "3eeafef49856de36",
            "src_ip": "251.71.156.29",
            "dst_ip": "15.232.103.129"
        },
        {
            "ticket_id": 1,
            "timestamp": "2017/06/14 12:51:03",
            "file_hash": "475bfd836c06221e",
            "src_ip": "204.108.217.70",
            "dst_ip": "235.0.152.20"
        },
        {
            "ticket_id": 2,
            "timestamp": "2017/06/03 06:03:13",
            "file_hash": "eab50c9ca5a93d0f",
            "src_ip": "31.13.251.15",
            "dst_ip": "27.58.104.112"
        },
        {
            "ticket_id": 3,
            "timestamp": "2015/06/15 16:49:10",
            "file_hash": "f849419bd47b7757",
            "src_ip": "251.71.156.29",
            "dst_ip": "235.0.152.20"
        },
        {
            "ticket_id": 4,
            "timestamp": "2015/04/22 18:29:14",
            "file_hash": "9387a2b957f63099",
            "src_ip": "31.13.251.15",
            "dst_ip": "15.232.103.129"
        },
        {
            "ticket_id": 5,
            "timestamp": "2015/03/08 11:13:26",
            "file_hash": "add6f36506e236d1",
            "src_ip": "251.71.156.29",
            "dst_ip": "136.78.113.43"
        },
        {
            "ticket_id": 6,
            "timestamp": "2016/12/23 22:14:01",
            "file_hash": "18ffd95e7b294af7",
            "src_ip": "204.108.217.70",
            "dst_ip": "124.238.255.184"
        },
        {
            "ticket_id": 7,
            "timestamp": "2017/08/31 19:20:57",
            "file_hash": "320167a7f0ddbe1e",
            "src_ip": "7.70.183.95",
            "dst_ip": "174.236.95.231"
        },
        {
            "ticket_id": 8,
            "timestamp": "2015/06/19 00:52:15",
            "file_hash": "9387a2b957f63099",
            "src_ip": "251.71.156.29",
            "dst_ip": "173.94.17.124"
        },
        {
            "ticket_id": 9,
            "timestamp": "2016/02/05 03:37:34",
            "file_hash": "3eeafef49856de36",
            "src_ip": "204.108.217.70",
            "dst_ip": "15.232.103.129"
        }
    ]
}`

![]{img\desrouleaux.png}
