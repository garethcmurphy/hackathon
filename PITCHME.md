---?color=#7E317B

## PaNOSC WP3 Hackathon

Gareth Murphy
@garethcmurphy

---

## Install Prerequisites

https://www.brew.sh

```bash
brew install git
brew install node
```

---

## Install common-api

```bash
git clone https://github.com/panosc-eu/common-api.git
cd common-api
npm install
npm start
```

---

## View Explorer

- Go to
  http://localhost:3000/explorer
- Click DatasetController -> Get -> Try it Out
- Change limit to 10
- Click Execute

---

## Create dataset

- POST

---

## Create unit test

```python
    it('retrieves datasets with H20,  pressure > 100', async () => {
      find.resolves(aListOfDatasets);
      const details = await controller.find({
        where: {and: [
            {'pressure.value': {gt: 100}}, 
            {sample: 'water'}
            ]
            },
      });
      console.log(details);
      expect(details).to.eql(aListOfDatasets);
      sinon.assert.called(find);
    });
```

@[1-3]
@[4,8]
@[9-11]

---
