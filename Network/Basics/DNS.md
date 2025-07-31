#### 1. DNS queries

DNS query is also known as a DNS request. So, it is a request for information that is sent from the user’s computer to ask for the IP address to a DNS server. This means the DNS client is querying the DNS server to get the IP address, related to that domain.

Three types of queries occurs in DNS query:

- **Recursive Query:** Recursive query is a type of query in which the DNS server will do all the job of answering the users. In recursive query DNS server querying to the other DNS server on behalf of the user. When the user requesting by asking name to the server, the server performs complete translation and the user directly gets the IP address of the domain.
- **Iterative Query:** In an iterative query, the user can request repeatedly to the different DNS servers for resolution. It means iterative DNS query is a request for a website or URL, DNS server responds with the IP address, if the server does not have the requested IP address then request forwarded to other DNS server.
- **Non-Recursive Query:** The non-recursive query is a query in which the DNS Resolver already knows the answer. That either immediately returns the DNS records or queries the name server which is authoritative for the records, because that stored in local cache, immediate response to be given to the user.

#### 2. DNS Servers

DNS servers convert domain names into IP addresses. It takes request from human and converts that into machine IP addresses that make easier to reach the origin server.

- **DNS Resolver:** DNS resolver is also called a recursive resolver, it converts hostname into IP address which is machine friendly. This server is designed to receive queries from web browsers and other applications. This resolver receives a hostname in the form of www.sample.com and also responsible for tracking the IP address for that hostname.
- **DNS Root Server:** Root servers are the DNS name servers that are operated in the root zone, root zone is the stored record of queries so that server can directly answer the query from the root zone or cache within the root zone. The DNS uses 13 DNS servers and that is based on a constraint of Internet Protocol version 4.
- **Authoritative Name Server:** The authoritative name server is the higher level in DNS. The DNS server is the ‘authoritative’, the authoritative name is given to the specific hostname because it holds the up-to-date information about that hostname.

#### 3. DNS Records

DNS server created a DNS record to give important information about the domain or hostname and its current IP address.

The common DNS record types are –
1. **A Record (Address Record)**
    - **Purpose**: Maps a domain to an IPv4 address.
    - **Example**:
        - `example.com. IN A 93.184.216.34`
        - This record links "example.com" to the IPv4 address "93.184.216.34".
2. **AAAA Record (IPv6 Address Record)**
    - **Purpose**: Maps a domain to an IPv6 address.
    - **Example**:
        - `example.com. IN AAAA 2606:2800:220:1:248:1893:25c8:1946`
        - This record links "example.com" to the IPv6 address "2606:2800:220:1:248:1893:25c8:1946".
3. **CNAME Record (Canonical Name Record)**
    - **Purpose**: Redirects one domain name to another. Often used for subdomains.
    - **Example**:
        - `www.example.com. IN CNAME example.com.`
        - This record makes "www.example.com" an alias for "example.com", so visitors to "www" are directed to the same IP address as "example.com".
4. **MX Record (Mail Exchange Record)**
    - **Purpose**: Directs email to the correct mail server for a domain.
    - **Example**:
        - `example.com. IN MX 10 mail.example.com.`
        - This record directs email for "example.com" to "mail.example.com" with a priority value of 10.
5. **PTR Record (Pointer Record)**
    - **Purpose**: Enables reverse DNS lookups, mapping IP addresses to domain names.
    - **Example**:
        - `34.216.184.93.in-addr.arpa. IN PTR example.com.`
        - This record maps the IP address "93.184.216.34" back to the domain name "example.com".
6. **TXT Record (Text Record)**
    - **Purpose**: Stores text-based data, often for verification or security purposes (e.g., SPF, DKIM, DMARC).
    - **Example**:
        - `example.com. IN TXT "v=spf1 include:_spf.google.com ~all"`
        - This record is used to specify an SPF (Sender Policy Framework) rule that allows Google's mail servers to send emails on behalf of "example.com".
7. **NS Record (Name Server Record)**
    - **Purpose**: Specifies the authoritative name servers for a domain.
    - **Example**:
        - `example.com. IN NS ns1.example.com.`
        - This record points to "ns1.example.com" as the authoritative name server for the domain "example.com".
8. **SRV Record (Service Record)**
    - **Purpose**: Defines the services and ports used by specific applications within a domain.
    - **Example**:
        - `_sip._tcp.example.com. IN SRV 10 60 5060 sipserver.example.com.`
        - This record indicates that the SIP (Session Initiation Protocol) service for "example.com" is provided by "sipserver.example.com" on port 5060, with a priority of 10 and a weight of 60.
