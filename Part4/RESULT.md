# Results

The magic number is a different one each time. The first thread is allowed some processing time, but does not quite finish its for loop. If it is interrupted after it has fetched the value of i, we will se an error. The other thread will run for a while. Then, when the first thread starts again, it will write back to the memory location the value of i as it was before the thread was interrupted, after adding 1 of course. This totally overwrites all the work done by the other thread, resulting in strange values for i.
