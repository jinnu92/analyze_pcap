# analyze_pcap
Generate the voice quality report. Support to extract the specific fields of the quality report.

DESCRIPTION:
analyze_pcap will generate the voice quailty report.
  
USAGE:

    analyze_pcap [ -h|--help ]
    
    analyze_pcap -r|--read <pcap file> [-r|--read] [-s_ip|--source_ip] [-s_port|--source_port] [-d_ip|--destination_ip] [-d_port|--destination_port] [-s|--ssrc] [-p|--payload] [-c|--codec] [-pk|--pkts] [-l|--lost] [-d|--delta] [-max_j|--max_jitter] [-mean_j|--mean_jitter] [-i|--problems] 

extended_usage=
    --help, -h              : Displays command usage.

    --read, -r <pcap file>  : Load a pcap file
    
    --source_ip, -s_ip      : Src IP addr

    --source_port, -s_port      : Port

    --destination_ip, -d_ip     : Dest IP addr

    --destination_port, -d_port : Port

    --ssrc, -s              : SSRC

    --payload, -p           : Payload

    --codec, -c             : Codec

    --pkts, -pk             : Pkts

    --lost, -l              : Lost

    --delta, -d             : Max Delta(ms)

    --max_jitter, -max_j    : Max Jitter(ms)

    --mean_jitter, -mean_j  : Mean Jitter(ms)

    --problems, -i          : Problems

EXAMPLES:

    analyze_pcap --help
    
    analyze_pcap -r G711.pcap
    
    analyze_pcap -r G711.pcap --source_ip 10.3.51.11 --source_port 35768 --codec
    
    analyze_pcap -r G711.pcap --source_ip 10.3.51.11 --source_port 35768 --max_jitter
            
Dependencies:

   apt-get install -y tshark
   
   yum install wireshark
