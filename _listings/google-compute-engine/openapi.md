---
swagger: "2.0"
x-collection-name: Google Compute Engine
x-complete: 1
info:
  title: Compute Engine
  description: creates-and-runs-virtual-machines-on-google-cloud-platform-
  contact:
    name: Google
    url: https://google.com
  version: v1
host: www.googleapis.com
basePath: /compute/v1/projects
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /{project}/aggregated/vpnTunnels:
    get:
      summary: Get VPN Tunnels
      description: Retrieves an aggregated list of VPN tunnels.
      operationId: compute.vpnTunnels.aggregatedList
      x-api-path-slug: projectaggregatedvpntunnels-get
      parameters:
      - in: query
        name: filter
        description: Sets a filter expression for filtering listed resources, in the
          form filter={expression}
      - in: query
        name: maxResults
        description: The maximum number of results per page that should be returned
      - in: query
        name: orderBy
        description: Sorts list results by a certain order
      - in: query
        name: pageToken
        description: Specifies a page token to use
      - in: path
        name: project
        description: Project ID for this request
      responses:
        200:
          description: OK
      tags:
      - VPN Tunnel
  /{project}/regions/{region}/vpnTunnels:
    get:
      summary: Get VPN Tunnels
      description: Retrieves a list of VpnTunnel resources contained in the specified
        project and region.
      operationId: compute.vpnTunnels.list
      x-api-path-slug: projectregionsregionvpntunnels-get
      parameters:
      - in: query
        name: filter
        description: Sets a filter expression for filtering listed resources, in the
          form filter={expression}
      - in: query
        name: maxResults
        description: The maximum number of results per page that should be returned
      - in: query
        name: orderBy
        description: Sorts list results by a certain order
      - in: query
        name: pageToken
        description: Specifies a page token to use
      - in: path
        name: project
        description: Project ID for this request
      - in: path
        name: region
        description: Name of the region for this request
      responses:
        200:
          description: OK
      tags:
      - VPN Tunnel
    post:
      summary: Create VPN Tunnel
      description: Creates a VpnTunnel resource in the specified project and region
        using the data included in the request.
      operationId: compute.vpnTunnels.insert
      x-api-path-slug: projectregionsregionvpntunnels-post
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: project
        description: Project ID for this request
      - in: path
        name: region
        description: Name of the region for this request
      responses:
        200:
          description: OK
      tags:
      - VPN Tunnel
  /{project}/regions/{region}/vpnTunnels/{vpnTunnel}:
    delete:
      summary: Delete VPN Tunnel
      description: Deletes the specified VpnTunnel resource.
      operationId: compute.vpnTunnels.delete
      x-api-path-slug: projectregionsregionvpntunnelsvpntunnel-delete
      parameters:
      - in: path
        name: project
        description: Project ID for this request
      - in: path
        name: region
        description: Name of the region for this request
      - in: path
        name: vpnTunnel
        description: Name of the VpnTunnel resource to delete
      responses:
        200:
          description: OK
      tags:
      - VPN Tunnel
    get:
      summary: Get VPN Tunnel
      description: Returns the specified VpnTunnel resource. Get a list of available
        VPN tunnels by making a list() request.
      operationId: compute.vpnTunnels.get
      x-api-path-slug: projectregionsregionvpntunnelsvpntunnel-get
      parameters:
      - in: path
        name: project
        description: Project ID for this request
      - in: path
        name: region
        description: Name of the region for this request
      - in: path
        name: vpnTunnel
        description: Name of the VpnTunnel resource to return
      responses:
        200:
          description: OK
      tags:
      - VPN Tunnel
---