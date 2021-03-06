# NextID Postgres Extension

[![Build Status](https://travis-ci.org/wellmart/pg-nextid.svg?branch=master)](https://travis-ci.org/wellmart/pg-nextid)
![Version](https://img.shields.io/badge/version-0.1.0-blue)
[![Software License](https://img.shields.io/badge/license-MIT-blue.svg?style=flat)](LICENSE)

Postgres Extension for ID generation based on Instagram ID. check out the post: [instagram-engineering.com](https://instagram-engineering.com/sharding-ids-at-instagram-1cf5a71e5a5c).

## Requirements

Postgres Server and Dev tools.

## Installation

Use the C++ make to install extension direct in Postgres.

```bash
make install
make clean
```

## Usage

Create extension in your database:

```sql
CREATE EXTENSION nextid;
```

Generate ID with extension:

```sql
SELECT c_next_id(NEXTVAL('id_seq'), 1) FROM generate_series(1, 100);
```

## License

[MIT](https://choosealicense.com/licenses/mit/)
