## ParaAMR

This repository contains the dataset for our **ACL-2023 Area Chair Award** paper [ParaAMR: A Large-Scale Syntactically Diverse Paraphrase Dataset by AMR Back-Translation](https://arxiv.org/abs/2305.16585).

After uncompressing `ParaAMR_small.zip`, you will get `ParaAMR_small.json` with each line being a json object:

```JSON5
{
    "text": "all of these men can confirm that cheryl was not here when harry was killed.",
    "paraphrases": [
        {
            "para_text": "all these men can confirm that cheryl wasn't here when harry was killed.",
            "perplexity": 125.02737280513969
        },
        {
            "para_text": "cheryl was not here when harry was killed, which all these men could confirm.",
            "perplexity": 96.61560039297649
        },
        ...
        {
            "para_text": "harry was the one killed when cheryl wasn't here, which is confirmed by all of these men.",
            "perplexity": 91.92300008948598
        }
    ]
}
```
There are 177,410 lines in total. This is a subset of ParaAMR that we are using for analysis and running experiments.
We will release the full set of ParaAMR, which contains 15,543,606 lines in total, as soon as possible.
Note that the source text comes from [ParaNMT](https://github.com/jwieting/para-nmt-50m) and we generate the paraphrases by AMR-back-translation. 
The perplexity is calculated based on [GPT-2](https://huggingface.co/docs/transformers/en/model_doc/gpt2).
Please check more details in our paper.

If you find that the code is useful in your research, please consider citing our paper.

    @inproceedings{acl2023paraamr,
        author    = {Kuan-Hao Huang and Varun Iyer and I-Hung Hsu and Anoop Kumar and Kai-Wei Chang and Aram Galstyan},
        title     = {ParaAMR: A Large-Scale Syntactically Diverse Paraphrase Dataset by AMR Back-Translation},
        booktitle = {Proceedings of the 61st Annual Meeting of the Association for Computational Linguistics (ACL)},
        year      = {2023},
    }


## Security

See [CONTRIBUTING](CONTRIBUTING.md#security-issue-notifications) for more information.

## License

This library is licensed under the CC-BY-NC License.

