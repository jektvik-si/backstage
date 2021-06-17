## API Report File for "@backstage/plugin-graphiql"

> Do not edit this file. It is a report generated by [API Extractor](https://api-extractor.com/).

```ts

import { ApiRef } from '@backstage/core-plugin-api';
import { BackstagePlugin } from '@backstage/core-plugin-api';
import { ErrorApi } from '@backstage/core-plugin-api';
import { IconComponent } from '@backstage/core';
import { OAuthApi } from '@backstage/core-plugin-api';
import { RouteRef } from '@backstage/core-plugin-api';

// @public (undocumented)
export type EndpointConfig = {
    id: string;
    title: string;
    url: string;
    method?: 'POST';
    headers?: {
        [name in string]: string;
    };
};

// @public (undocumented)
export type GithubEndpointConfig = {
    id: string;
    title: string;
    url?: string;
    errorApi?: ErrorApi;
    githubAuthApi: OAuthApi;
};

// @public (undocumented)
export const GraphiQLIcon: IconComponent;

// @public (undocumented)
export const GraphiQLPage: () => JSX.Element;

// @public (undocumented)
const graphiqlPlugin: BackstagePlugin<{}, {}>;

export { graphiqlPlugin }

export { graphiqlPlugin as plugin }

// @public (undocumented)
export const graphiQLRouteRef: RouteRef<undefined>;

// @public (undocumented)
export type GraphQLBrowseApi = {
    getEndpoints(): Promise<GraphQLEndpoint[]>;
};

// @public (undocumented)
export const graphQlBrowseApiRef: ApiRef<GraphQLBrowseApi>;

// @public (undocumented)
export type GraphQLEndpoint = {
    id: string;
    title: string;
    fetcher: (body: any) => Promise<any>;
};

// @public (undocumented)
export class GraphQLEndpoints implements GraphQLBrowseApi {
    // (undocumented)
    static create(config: EndpointConfig): GraphQLEndpoint;
    // (undocumented)
    static from(endpoints: GraphQLEndpoint[]): GraphQLEndpoints;
    // (undocumented)
    getEndpoints(): Promise<GraphQLEndpoint[]>;
    static github(config: GithubEndpointConfig): GraphQLEndpoint;
}

// @public (undocumented)
export const Router: () => JSX.Element;


// (No @packageDocumentation comment for this package)

```