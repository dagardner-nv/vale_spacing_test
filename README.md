This is the smallest reproducible block of text that triggers the issue. Issue has been observed with versions 3.6.1 and 3.7.0

1. This stage keeps a moving window of logs on a per user basis
   * These logs are saved to disk to reduce memory requirements between logs from the same user
1. It repeats the necessary logs to properly calculate log dependent features.
   * To support all column feature types, incoming log messages can be combined with existing history and sent to downstream stages.

When `max_history` is a `str` it's assumed to represent a duration which is able to be parsed by `pandas.Timedelta`.
