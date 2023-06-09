# PhD Dissertation Artifact: A Blend of Intersection Types and Union Types

This repository contains a part of the artifact associated
with my PhD dissertation. In particular, it contains the
Coq formalization of `Chapter 4`, `Chapter 5`, and `Appendix A`.
Note that `Chapter 3` and `Chapter 6` (each) have a different
repository for the artifact. Details for `Chapter 3` and `Chapter 6`
can be found in their respective repos.

Correspondence of folders and thesis chapters in this
repository is:

| Folder    | Description                                                          | Reference in thesis |
|:----------|:---------------------------------------------------------------------|:--------------------|
| chap4     | Revisiting Disjointness (Updated disjointness with polymorphism)     | Chapter 4           |
| chap5     | Togetherness: Switches and Merges                                    | Chapter 5           | 
| appendixA | Alternative Disjointness (Another variant of disjointness with COST) | Appendix A          |


Description of each folder is:

## Chapter 4 (chap4)

The folder `chap4` consists of two sub-folders:

| Sub-folder         | Description                                                                | Reference in thesis |
|:-------------------|:---------------------------------------------------------------------------|:--------------------|
| chap4/unioninter   | Updated disjointness with intersection and union types                     | Section 4.1         |
| chap4/disjointpoly | Updated disjointness with intersection types, union types and polymorphism | Section 4.2         | 

Each folder contains two files named `syntax` and `typing`.
Description of each file is:

| File     | Description                       |
|:---------|:----------------------------------|
| syntax.v | Contains types and subtyping      |
| typing.v | Contains type-safety proofs       |

Correspondence of important lemmas in thesis and artifact is:

| Lemma in Thesis | Coq File              | Lemma in Coq file        |
|:----------------|:----------------------|:-------------------------|
| Lemma 4.1       | unioninter/syntax.v   | UO_or_US                 |
| Lemma 4.2       | unioninter/syntax.v   | Disj2_sound              |
| Lemma 4.3       | unioninter/syntax.v   | Disj2_Complete_size      |
| Lemma 4.4       | unioninter/syntax.v   | sub_refl                 |
| Lemma 4.5       | unioninter/syntax.v   | sub_transitivity         |
| Theorem 4.6     | unioninter/typing.v   | preservation             |
| Theorem 4.7     | unioninter/typing.v   | progress                 |
| Theorem 4.8     | unioninter/typing.v   | determinism              |


| Lemma in Thesis | Coq File              | Lemma in Coq file        |
|:----------------|:----------------------|:-------------------------|
| Lemma 4.9       | disjointpoly/typing.v | sub_disjoint3            |
| Lemma 4.10      | disjointpoly/syntax.v | sub_refl                 |
| Theorem 4.11    | disjointpoly/syntax.v | sub_transitivity         |
| Theorem 4.12    | disjointpoly/typing.v | preservation             |
| Theorem 4.13    | disjointpoly/typing.v | progress                 |
| Theorem 4.14    | disjointpoly/typing.v | determinism              |
| Lemma 4.15      | disjointpoly/typing.v | typing_through_subst_te  |
| Lemma 4.16      | disjointpoly/typing.v | sub_disjoint3            |
| Lemma 4.17      | disjointpoly/typing.v | disj_subst               |
| Lemma 4.18      | disjointpoly/typing.v | typing_narrowing         |
| Lemma 4.19      | disjointpoly/typing.v | sub_narrowing_aux        |
| Lemma 4.20      | disjointpoly/typing.v | disj_narrowing           |
| Lemma 4.21      | disjointpoly/typing.v | typing_weakening         |
| Lemma 4.22      | disjointpoly/typing.v | sub_weakening            |
| Lemma 4.23      | disjointpoly/typing.v | disj_narrowing           |
| Lemma 4.24      | disjointpoly/typing.v | UO_sub_union             |
| Lemma 4.25      | disjointpoly/typing.v | US_wft                   |
| Lemma 4.26      | disjointpoly/typing.v | disj_sym                 |
| Lemma 4.27      | disjointpoly/typing.v | val_check_disjoint_types |

## Chapter 5 (chap5)

This folder contains Coq formalization corresponding to `chapter 5` in thesis.
Description of each file is:

| File                | Description                       | Reference in thesis |
|:--------------------|:----------------------------------|:--------------------|
| chap5/syntax.v      | Contains types and subtyping      | Section 5.1         |
| chap5/typing.v      | Contains type-safety proofs       | Section 5.2         |
| chap5/equivalence.v | Completeness to Dunfield's system | Section 5.3         |

Correspondence of important lemmas in thesis and artifact is:

| Lemma       | Coq File      | Lemma in Coq file            |
|:------------|:--------------|:-----------------------------|
| Lemma 5.1   | syntax.v      | sub_refl                     |
| Lemma 5.2   | syntax.v      | sub_transitivity             |
| Theorem 5.3 | typing.v      | tred_preservation_infer      |
| Theorem 5.4 | typing.v      | tred_progress_dir            |
| Theorem 5.5 | typing.v      | preservation                 |
| Theorem 5.6 | typing.v      | progress                     |
| Lemma 5.7   | typing.v      | pexpr_reduce_under_arrow_abs |
| Lemma 5.8   | typing.v      | getInTypeSup                 |
| Lemma 5.9   | typing.v      | getInTypeInv'                |
| Lemma 5.10  | typing.v      | dynSemanticsProgress         |
| Lemma 5.11  | equivalence.v | dt_complete                  |


## Appendix A (appendixa)

This folder contains the Coq formalization associated with
Appendix A in thesis. The file `appendixa/syntax` contains
types, subtyping, and a variant of disjointness based on COST.

Correspondence of important definitions and lemmas is:

| Lemma       | Coq File | Lemma in Coq file            |
|:------------|:---------|:-----------------------------|
| Lemma A.1   | syntax.v | sub_refl                     |
| Lemma A.2   | syntax.v | sub_transitivity             |
| Lemma A.3   | typing.v | cost_sound                   |
| Lemma A.4   | typing.v | cost_complete                |
| Lemma A.5   | syntax.v | disj_sound and disj_complete |
| Theorem 5.6 | typing.v | preservation                 |
| Theorem 5.7 | typing.v | progress                     |
| Theorem 5.8 | typing.v | determinism                  |


# How to Run?

We provide two alternatives for building the artifact:

1. Build From Scratch
2. Docker Image

## 1) Build From Scratch

#### Dependencies

Artifact is compiled with **Coq version 8.13.2**. We recommend the same for the
sake of consistency. Detailed instructions of installing `Coq` are available
at: `https://coq.inria.fr/opam-using.html`.

Artifact also depends on two external libraries:

#### a) Metalib.
Detailed installation instructions of Metalib are available
at: `https://github.com/plclub/metalib`.
**Recommended Metalib version is coq8.10**. This version compiles with Coq 8.13.2.

#### b) TLC
Detailed TLC installation instructions are available
at: `https://github.com/charguer/tlc`.
We recommend TLC installation via `opam`:
`opam install -y coq-tlc.20210316`.

Note that we recommend TLC version `20210316`.

### Running the artifact

Clone the repo using command: `git clone https://github.com/baberrehman/phd-thesis-artifact`

We provide a `Makefile` in `coq` folder of each chapter and section.
Open a terminal in `coq` folder and
run `make` command. This command will compile all the Coq files. Reader may look into
each coq file to verify the claims using their preferred editor.

## 2) Docker Image

Alternatively, we also provide a dockerfile in this artifact with all the dependencies
installed. You may simply build and run the docker image using the provided dockerfile.

*Please make sure that the docker is already installed on your system to follow this track.*

1. Clone this repo using command: `git clone https://github.com/baberrehman/phd-thesis-artifact`
2. Change directory to the root of the artifact: `cd phd-thesis-artifact`
3. Build docker image: `sudo docker build -t blendthesis .` (**Note that . is a part of command**)
4. Run the docker container with an interactive shell: `sudo docker run -it blendthesis`
5. This will open the home directory of the artifact's docker container
7. Build the artifact by running the make command inside the `Coq` folder for each chapter/section: `make`
8. `vim` is pre-installed in the docker container to look into the files

Note that the docker container clones the same repo in itself. Reader may directly
look into the code of this repo using their preferred editor as an easier option.

