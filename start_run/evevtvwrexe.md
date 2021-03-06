### evevtvwr.exe {#evevtvwr-exe}

了解事件日志选项使用&quot;事件查看器&quot;，您可以为每一种事件日志定义日志参数。要定义参数，请右键单击控制台树中的日志，然后单击&quot;属性&quot;。在&quot;常规&quot;选项卡上，您可以设置日志大小的最大值并指定是否在某段时间内改写或存储事件。

默认的日志策略为：如果日志已满，则删除至少在七天以上的最早的事件，为新事件留出空间。您可以对不同的日志自定义该策略或事件日志覆盖选项。

事件日志覆盖选项包括以下内容。

使用                     用途

按需要改写事件:          当日志已满时继续写入新的事件。每个新事件替换日志中时间最长的事件。该选项对维护要求低的系统是一个不错的选择。

改写久于[x] 天的事件: 保留位于指定改写事件的天数之前的日志。默认值为 7 天。如果您想每周存档日志文件，该选项是最佳选择。该策略将丢失重要日志项的几率降到最小，同时保持日志的合理大小。

不改写事件:                 手动而不是自动清除或存档日志。只有在您无法承受丢失事件时才选中该选项（例如，特别强调安全性的站点的安全日志）。

按需要覆盖事件(旧事件优先)。也就是说，当日志文件达到上限时，会把一些旧的日志文件记录删除掉，以存储新的日志信息。这个选项跟2003操作系统类似。不过这里需要注意的是，如果选择这个选项的话，那么对于日志空间的大小需要特别的注意。如在Windows7 中有一个防火墙日志，如果系统启用了防火墙，而且这台操作系统网络通信比较频繁的话，那么这个日志空间的上限就需要设置的大一点。否则的话，当系统遇到故障时，可能无法查到一些有用的信息，因为这些信息已经被覆盖掉了。

不覆盖事件。当日志文件达到上限值之后，系统不会继续记录新的事件信息。需要系统管理员手工清楚日志文件后，系统才会记录记录日志信息。显然这不是很好的处理方式。除非有特殊的需要，最好不要选择这个选项。

日志满时将其存档，不覆盖事件。这个选项是2003操作系统中没有的，在Windows7操作系统中新增加的选项。笔者个人认为，这个选项非常实用。对于一些稳定性要求比较高档服务器，对一年甚至更长时间的日志进行存档是必须的。如一些文件访问的审核日志等等。如果选择了这个选项，那么到日志文件的大小达到上限时，操作系统不会覆盖原有的日志记录。而是先把旧的日志记录进行存档，然后再利用新的日志信息来覆盖旧的日志信息。此时如果系统管理员需要查看比较旧的日志信息，如去年这个时候的日志，那么就可以去查看相关的归档文件，这确实是Windows7种一个很有吸引力的改进。