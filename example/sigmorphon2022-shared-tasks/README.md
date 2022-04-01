# [SIGMORPHON 2022 Shared Task 0](https://github.com/sigmorphon/2022InflectionST) Baseline



### Training from Scratch

Run input-invariant transformer [(Wu and Cotterell, 2019)](https://arxiv.org/abs/2005.10213) or the vanilla transformer [(Vaswani et al., 2017)](https://arxiv.org/abs/1706.03762).
```bash
model=tagtransformer # input-invariant transformer, or `model=transformer` the vanilla transformer
# Large training
for lang in ang ara asm evn got heb hun kat khk kor krl lud non pol poma slk tur vep
    bash example/sigmorphon2022-shared-tasks/task0-trm.sh $lang $model large
done

# Small training
for lang in ang ara asm bra ckt evn gml goh got guj heb hsb hsi hun itl kat ket khk kor krl lud mag nds non pol poma sjo slk tur vep
    bash example/sigmorphon2022-shared-tasks/task0-trm.sh $lang $model small
done
```