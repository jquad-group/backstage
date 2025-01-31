## API Report File for "@backstage/plugin-stack-overflow-backend"

> Do not edit this file. It is a report generated by [API Extractor](https://api-extractor.com/).

```ts
/// <reference types="node" />

import { Config } from '@backstage/config';
import { DocumentCollatorFactory } from '@backstage/plugin-search-common';
import { IndexableDocument } from '@backstage/plugin-search-common';
import { Logger } from 'winston';
import { Readable } from 'stream';

// @public
export interface StackOverflowDocument extends IndexableDocument {
  // (undocumented)
  answers: number;
  // (undocumented)
  tags: string[];
}

// @public
export class StackOverflowQuestionsCollatorFactory
  implements DocumentCollatorFactory
{
  // (undocumented)
  execute(): AsyncGenerator<StackOverflowDocument>;
  // (undocumented)
  static fromConfig(
    config: Config,
    options: StackOverflowQuestionsCollatorFactoryOptions,
  ): StackOverflowQuestionsCollatorFactory;
  // (undocumented)
  getCollator(): Promise<Readable>;
  // (undocumented)
  protected requestParams: StackOverflowQuestionsRequestParams;
  // (undocumented)
  readonly type: string;
}

// @public
export type StackOverflowQuestionsCollatorFactoryOptions = {
  baseUrl?: string;
  apiKey?: string;
  requestParams: StackOverflowQuestionsRequestParams;
  logger: Logger;
};

// @public
export type StackOverflowQuestionsRequestParams = {
  [key: string]: string | string[] | number;
};
```
