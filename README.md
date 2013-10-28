# php json RPC client


Simple php class that implements json RPC client over raw tcp, designed to be used with go "net/rpc/jsonrpc" package.

Socket connections are opened following lazy pattern and are closed during object destruction.

### JsonRpcClient($address, $port)

create a new connection

    $connection = new JsonRpcClient($address, $port);

### Call($method, $params)

get response for given method and params

    $response = $connection->Call($method, $params);
